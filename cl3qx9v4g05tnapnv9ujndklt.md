# Basics Of Linux

Hey everyone, Maharshi this side and in this blog we're going to cover about **Linux**. But wait you also think Linux as *tough and difficult* 🤐 don't worry few times ago I feels the same but believe in time and process, you'll too love the Linux much 💯. Ok so Let's deep into this new world from **Scratch**

# Starting of System 💻

Aren't you too think that what happens when we starts our system !? is there any kind of rocket science is behind this ....? Let's understand this first.

1. BIOS (Basic Input and Output System) is a firmware which is present inside of a small chip and that chip is present inside the mother board.
2. When the computer is turned on, the software inside the BIOS are executed. These software perform certain checks such as if the memory is loaded, how many drives are present so as to ensure that the system is ready to launch the Operating System (OS).
3. After the checks are performed, the boot-loader is loaded to the memory, which is what initiates the Operating System.
4. This is what happens when you start the computer.  

# What is an Operating System ?
 > It is just a simple *software* that is responsible for managing and operating a computing device.

Now, a question arise that what things are responsible to differentiate a normal software and a OS. `So, let's take a glance into the list of things that every software needs :`

1. **Kernel**
> Core of any Operating System & it has complete control over everything in the system. It can control-memory, CPU time of any software. It facilitates the interaction between a software & hardware.

2. **File System**
> Method or a data structure that the OS uses to store & retrieve data in the memory.

3. **User Interface**
> Either CLI (Command Line Interface) or GUI (Graphical User Interface)

4. **Should be able to manipulate data based on commands**

# Why Linux ?

**Linux is like : The more you get to know about it, the more you love it❤.**
but why people loves Linux the most ....? the reason behind this is :

➡ *Linux is Open Source* you're literally able to contribute into it and generally developers are fixes bugs often unlike windows where large number of bugs are dealt at once for commercial purpose.

➡ Support almost all programming language

➡ Terminal is superior to CMD (windows' command terminal)

➡ For SSH-ing into the server that you would host locally / remotely 

➡ Bash scripting is possible. This is great for scripting, cron jobs, while using docker for containerization and for devops purposes.


And much more......

Also, Linux has various flavors of operating systems in which each flavor of Linux distro (distribution) is meant for a particular purpose.
![linux-distro-stickers.webp](https://cdn.hashnode.com/res/hashnode/image/upload/v1653745573577/6FYQqSU62.webp align="center")

**Some popular among them are :**

- Ubuntu Desktop: General Purpose

- Kali Linux: Hacking Purpose

- Parrot OS: Hacking Purpose

- Red Hat Enterprise Linux: Enterprise Purpose

- Arch Linux: Geeky People and Advance Users

- BlackArch Linux: Penetration Testing

Like this, depending on purpose we can select one particular Linux Distro/ Flavor/ Distribution.

# What is Terminal ?

> Shortcut : `ctrl + alt + t`

> Shortcut for increasing terminal's size : `ctrl + shift + +`

In simple terms, terminal is a program which helps us to interact with the computer without using much of the graphical interface. It is preferred over the Graphical User Interface as it saves a lot of resources from being used. A GUI needs more resources because some elements such as icons, cursor, drivers need to be loaded while working with it. Additionally, it eliminates the need to open file manager for basic work like moving or deleting files while working in IDEs due to the integration of the terminal into the IDEs.


![terminal.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1653746061138/m0Wg4Gc7b.gif align="center")


# The Shell


- 
It is a Command Line interpreter & it executes each and every *command line by line*


- 
It's also like a program that takes your command from keyboard and sends them to the Operating System to perform.



![shell.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1653747982558/oxZuj5Fb0.png align="center")


 - Most of the Shell by default use `Bash` as their programming language.

# Shell Format


```shell
username@hostname :~$
``` 
> here "tilde"(~) means `home directory` or the directory in which you are in.

> Also, "Doller" ($) means `after this you can start typing`

> Username - name of the logged-in user.

> Hostname - name of the host, that hosts this Linux server. It is generally the name of your system. 



# Tree Hierarchy for Directories !

The hierarchy present in the image is called Tree-hierarchy, which is what is followed in all Linux-distributions ⤵


![Blog_tree_-removebg-preview.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1653758006203/2XMa8gfH4.png align="left")
- Files are present in `Hierarchical` order in a system having any Operating System
- In Linux folder are termed as **Directory**
- The first or top directory from where it all starts is known as `root directory`.
- Root denoted is always represend with **Slash** `/`.
- Inside the root directory, Home directory is present.
- **Path** : home/username is represented by '~' . Here the term 'username' represents the different users present inside the home directory.

# Hello to Bash !

Whatever you write after the `"echo"` command, that will gonna print.


```bash
username@hostname:~$ echo Hello World !
Hello World !
``` 
`Example :`


![Blog Bash.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1653760460094/UrYLZe0JY.png align="left")


# Points to be Remember

1. Bash is a **case sensitive** so keep your eyes on the Syntax.

2. Try To avoid single quotes and double quotes because it has different meanings  
(' '/ " ").

3. Everything is all about Practice, so keep learning ✌🏼  


![linux.webp](https://cdn.hashnode.com/res/hashnode/image/upload/v1653760929828/0NjNkYhue.webp align="center")

# End Note
So that's all about my first blog in the series of "Linux" so all the basic process is covered in this one and from the next blog I'll going to post all the **Basic Commands of Linux** to you. Till then Thank you & make sure to comment down What should I improve and also what did you like the most about this blog !
Also you can follow me for update 
> Have a Nice day :)