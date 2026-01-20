---
title: "Keploy Assignment 1: Auto-Generating API Tests for a Spring Boot + Postgres App (Docker Compose)"
datePublished: Tue Jan 20 2026 13:47:24 GMT+0000 (Coordinated Universal Time)
cuid: cmkmnf0bz000502lb53of23dj
slug: keploy-assignment-1-auto-generating-api-tests-for-a-spring-boot-postgres-app-docker-compose
tags: postgresql, docker, apis, springboot, keploy, apitestautomation

---

Testing APIs manually is time-consuming, and writing integration tests from scratch can slow down development, especially when you’re building fast.

In this assignment, I integrated **Keploy** with a **Spring Boot REST API + PostgreSQL** application running via **Docker Compose**, recorded real API traffic, and generated test cases automatically.

This post covers the full workflow, end-to-end, so that beginners can follow it easily.

---

## What is Keploy?

**Keploy** is an API testing tool that automatically generates test cases by recording actual API calls (requests + responses).  
Instead of manually writing tests, you:

1. Start Keploy in **record mode**
    
2. Trigger API requests (via curl/Postman/UI)
    
3. Keploy captures traffic and saves it as test cases (YAML)
    
4. Run Keploy in **test/replay mode**
    
5. Keploy replays the recorded requests and validates responses
    

---

## Project Used in This Assignment

I integrated Keploy with a Java Spring Boot project named:

**employee-manager** (Spring Boot REST API)

### Tech stack

* Java (Spring Boot)
    
* PostgreSQL
    
* Docker + Docker Compose
    
* REST endpoints like:
    
    * `GET /api/employees`
        
    * `POST /api/employees`
        

---

## Environment Setup

### Prerequisites

Make sure you have:

* Docker installed
    
* Docker Compose installed
    
* Keploy CLI installed
    
* A working Spring Boot + DB project
    

Quick verification:

```plaintext
docker --version
docker compose version
```

---

## Step 1: Start Clean (Remove Old Containers)

This was one of the most important steps for avoiding unexpected issues.  
Old containers (especially Keploy-generated ones) can cause conflicts.

Go to the project directory:

```plaintext
cd /Users/maharshi/Downloads/samples-java/employee-manager
```

Now stop and remove containers:

```plaintext
docker compose -f docker-compose.yaml down --remove-orphans
docker rm -f javaApp postgres 2>/dev/null
docker rm -f $(docker ps -aq --filter "name=keploy") 2>/dev/null
rm -f docker-compose-tmp.yaml
```

Confirm everything is clean:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1768916637123/68bdf445-8a7a-41b0-9f7e-ece206ed4cf2.jpeg align="center")

---

## Step 2: Verify the App Works Without Keploy

Before recording anything, I ensured the application runs normally.

Start the project:

```plaintext
docker compose -f docker-compose.yaml up --build
```

Then, in a new terminal, test the API:

```plaintext
curl http://localhost:8081/api/employees
```

Expected response:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1768916090384/74e3bd3d-296e-4407-b224-7971e616554a.png align="center")

Once confirmed, stop containers:

```plaintext
docker compose -f docker-compose.yaml down
```

---

## Step 3: Record API Traffic with Keploy

Keploy works best when it starts the application itself, so I used Docker Compose mode.

### Start Keploy record mode

```plaintext
keploy record --cmd-type docker-compose --container-name javaApp --pass-through-ports 5432 \
-c "docker compose -f docker-compose.yaml up --build" --record-timer 2m
```

### What these flags mean

* `--cmd-type docker-compose` → app runs using docker-compose
    
* `--container-name javaApp` → name of the application container
    
* `--pass-through-ports 5432` → allow Postgres traffic (do not mock DB)
    
* `--record-timer 2m` → record traffic for 2 minutes
    
* `-c "docker compose ..."` → command Keploy uses to start the app
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1768916152378/862bd705-6bf7-4939-bbbe-0a4f13a5b236.jpeg align="center")

---

## Step 4: Hit API Endpoints During Recording

While Keploy was recording, I triggered API calls using `curl`.

### 1) GET employees

```plaintext
curl http://localhost:8081/api/employees
```

### 2) POST a new employee

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1768916505524/08281495-08e9-4f85-ad76-f23d326fc3e9.png align="center")

Example response:

```plaintext
{"id":2,"firstName":"Maharshi","lastName":"Sinha","email":"maharshi@gmail.com","timestamp":1768834869}
```

### 3) GET again

```plaintext
curl http://localhost:8081/api/employees
```

Example output:

```plaintext
[
  {"id":1,"firstName":"Maharshi","lastName":"Sinha","email":null,"timestamp":1768834800},
  {"id":2,"firstName":"Maharshi","lastName":"Sinha","email":"maharshi@gmail.com","timestamp":1768834869}
]
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1768916207601/a0e99cb8-22e7-48c9-9055-65ce46e862e5.jpeg align="center")

---

## Step 5: Confirm Keploy Generated Test Cases

After recording, Keploy stored test cases in the `keploy/` directory.

Check generated tests:

```plaintext
ls -R keploy/
```

In my case, Keploy created:

```plaintext
ls -R keploy/test-set-2/tests
```

Output:

```plaintext
test-1.yaml
test-2.yaml
```

---

## Step 6: Replay Tests Using Keploy

Now I replayed the recorded tests.

```plaintext
keploy test --cmd-type docker-compose --container-name javaApp --pass-through-ports 5432 \
-c "docker compose -f docker-compose.yaml up --build" --delay 60
```

### Why `--delay 60`?

Spring Boot + DB containers can take time to become ready.  
If the delay is too low, Keploy may fail with:

`keploy-agent did not become ready in time`

Increasing the delay helps the agent and application initialize properly.

---

## Challenges I Faced (and How I Fixed Them)

### 1) `curl: (7) Failed to connect to` [`localhost`](http://localhost)

This happened when the containers were not running or the ports were mismatched.

Fix:  
Check containers:

```plaintext
docker ps
```

Also, confirm your port mapping in Docker Compose.  
Example: if you mapped `8081:8080`, your curl must use `8081`.

---

### 2) `unknown flag: --delay` in record mode

I mistakenly used `--delay` with `keploy record`.

Fix:  
Use `--record-timer` for record mode:

```plaintext
--record-timer 2m
```

---

### 3) Orphan containers/temp compose conflicts

Keploy generates an internal compose file:

📄 `docker-compose-tmp.yaml`

Sometimes this caused conflicts between runs.

Fix:  
Remove it before retrying:

```plaintext
rm -f docker-compose-tmp.yaml
```

---

## How Keploy Works Internally (What I Observed)

From Keploy logs and behavior, I learned:

### Keploy creates a temporary docker-compose file

During record/test mode, Keploy modifies the compose setup internally and creates:

`docker-compose-tmp.yaml`

This helps Keploy attach its agent and proxy layer to the application network.

### Keploy captures traffic and stores YAML test cases

Each API request becomes a YAML file containing:

* request method + URL
    
* headers + body
    
* response status + body
    

These are stored inside:

`keploy/test-set-x/tests`

### Replay mode validates responses

During replay, Keploy sends the same requests again and compares:

* recorded response vs current response
    

This makes it useful for regression testing.

---

## Final Outcome

By the end:

* I successfully integrated Keploy with a Spring Boot + Postgres project
    
* Keploy recorded real API calls and generated YAML test cases
    
* I learned how Keploy uses a proxy + agent and creates a temp compose file internally
    
* I was able to replay recorded tests for validation
    

---

## 🔗 GitHub Repository

📌 Repository link:  
[`https://github.com/maharshi-sinha/employee-manager`](https://github.com/maharshi-sinha/employee-manager)

---

## 🎯 Conclusion

Keploy is a practical tool for quickly generating API tests from real traffic, especially useful when you want fast regression coverage without manually writing integration tests.

If you’re new to Keploy, the best workflow is:

1. Run app normally → confirm curl works
    
2. Record with Keploy
    
3. Hit endpoints
    
4. Confirm YAML test cases
    
5. Replay tests with enough delay
    

---