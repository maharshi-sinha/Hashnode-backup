---
title: "Basics Of Dart Language (part 1)"
datePublished: Mon Dec 11 2023 11:55:10 GMT+0000 (Coordinated Universal Time)
cuid: clq0uwwmd000008kxgwv57iff
slug: basics-of-dart-language-part-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698788831779/a2b8df8b-a9a8-42cd-b9ab-3055db2b238b.png
tags: dart, flutter, dart-programming-tutorial, dart-for-beginners

---

Hello, amazing readers! hope you all doing amazing and learning something new every day. In the last blog, I covered all the basics of Dart Language, like the history of Dart, some learning resources and whatnot. The last blog was quite theoretical and if we are talking about any language then how can we ignore codes after all, it is the only thing that we developers know.

In this blog, I'll mainly cover the most important and basic topics to start with Dart language or you can say these will be selectively those types of topics which are must to know while working in Dart Language.

## Hello World!

If you're learning programming then we all know the value of "Hello World" isn't it? Just kidding, in the previous blog I already covered the code structure of Dart Language, but in this one, I'm again starting everything from the start so not overwriting the same thing again I'll try to explain both the code structure and printing "hello world" through the single example.

In Dart, the entry point is the `main()` function. You might be unfamiliar with what a function is at this point; that’s okay. For now, just remember that when you run a Dart program, the compiler looks for the `main()` function and executes the code written in that function. If `main()` is not found, you will get an error and your application won’t run. The code you write in `main()` is encapsulated in curly brackets (`{}`). Let’s look at the general syntax below.

The keyword `main` is followed by a set of parentheses (`()`) which is followed by an opening curly bracket (`{`). Start writing your code from the next line and when you’re done, insert a closing curly bracket. Here we're printing "Hello World" (`}`) in the line after the last line of your code.

```dart
void main(){
print ("Hello World"); //prinitng via using "print"
}
```

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">For printing anything we can also use `stdout`</div>
</div>

```dart
void main(){
stdout.write ("Hello World"); //prinitng via using "stdout"
}
```

> Both will give the same outputs as "Hello World"

## Taking Value from the User

Here in Dart, for taking input from the console we need to import a library, named `dart:io` from the libraries of Dart.

Let's understand this topic by the code itself.

```dart
 import 'dart:io'; 
void main(){
  stdout.write("Enter your name: ");
  var name = stdin.readLineSync(); //declaring variable & taking values
  print("Welcome, $name"); //printing the output
//use can also use stdout here instead of print.
}
```

here we are using `stdin` class to take input from the user and that's how the output will be shown.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698823202980/c5225dc1-8525-4611-b1c5-1f6c7d878cb8.png align="center")

## Classes & Objects in Dart

**Dart keywords** are reserved words or terms in the Dart programming language that the compiler interprets differently.

> These keywords can’t be used as the name of a variable, class, or function.

Dart keywords are <mark>case-sensitive</mark> and must be defined properly.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698824533627/d5a57817-17a3-4ced-b5bb-50226afa7200.png align="center")

The Dart programming language has a total of <mark>61 keywords</mark>.

| assert | export | interface | sync |
| --- | --- | --- | --- |
| async | extend | is | this |
| await | extension | library | throw |
| break | external | mixin | true |
| case | factory | new | try |
| class | final | catch | false |
| null | typedef | on | var |
| const | finally | operator | void |
| continue | for | part | while |
| covariant | function | rethrow | with |
| default | get | return | yield |
| deferred | hide | set | do |
| if | show | dynamic | implements |
| static |  |  |  |

---

## Creating Objects:

* Objects are the instance of the class and they are declared by using a ***<mark>new</mark>*** keyword followed by the class name.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698859347813/f4afa339-5326-4d7b-9803-765c142fbf04.png align="center")

```dart
var object_name = new class_name([ arguments ]);
```

* **new** is the keyword used to declare the instance of the class
    
* **object\_name** is the name of the object and its naming is similar to the variable name in dart.
    
* **class\_name** is the name of the class whose instance variable is been created.
    

**arguments** are the input that needs to be passed if we are willing to call a constructor.

---

## Var & Dynamic

<mark>Var and Dynamic</mark> both are dynamically typed data types, but var is dynamically typed until it has not assigned any value when we store any value in var it will be its data type and if we try to change it will through an error.

let’s understand this concept with an example.

```dart
var name = "flutter";
//it'll automatically understand that you're using a string variable
name = "dart"; // no error
name = 7; // error
//here it'll throw a error because your first initialization was a STRING!
```

* Example 2
    
    ```dart
    var rollno = 11;
    ```
    
    here you've initialized rollno with an int so every time it'll take int value only.
    

---

## **Dynamic Var**

Dynamic var is also the same as the var but the only major difference between both of them is, that in "dynamic var" you don't have to pre-define the value earlier and you can override the values. Let's understand this via an example:

```dart
var section; //here you aren't initializing anything so,
section = "D"; //dynamic
section = 8; //dynamic
```

here it won't throw any error as it is overriding the values because we are not pre-defining the values at the start. Let's clarify this more by taking another example:

```dart
dynamic section;
section = "D"; //string
section = 11; //int
section = false; //bool
```

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">you can also do the same thing by replacing "var" with "dynamic", don't get confused as to why I'm using dynamic in this example.</div>
</div>

---

## Functions

In Dart, a function is a reusable block of code that performs a specific task or set of tasks. Functions are a fundamental concept in programming, and they play a crucial role in structuring and organizing code.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698871590250/cd5febbb-a26e-4695-80c5-c5a437373d4f.png align="center")

```dart
void main(){
print("Hello World!");
var myC = myClass(); //class object instance
myC.printname(); //Function calling
}
class myClass{ //class
void printname(){
print("Hello Dart");
}
}
```

* Output
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698872788554/9bf37ec4-d7b3-4401-a842-15ed61df407c.png align="center")

---

▸ **Using the same thing multiple times!**

```dart
void main(){
print("Welcome to Flutter Series");
var myC = myClass(); 
myC.printname("Hope");
myC.printname("you're liking");
myC.printname("this series");
}
class myClass{ //class
void printname(String name){ //here we are using String
print(name);
}
}
```

Output of this code will be:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698873344211/9ba79665-7b3a-4f29-a79c-9c59c092b1a1.png align="center")

## Adding two numbers

* Example 2
    

```dart
void main(){
print("Welcome to Flutter Series");
var myC = myClass(); 
print (myC.Add(5,6));
print (myC.Add(200,300));
}
class myClass{ //class
int Add(int no1, int no2){
int sum = no1+no2;
return sum;
}
}
```

The output will be:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698873678719/58b5bfa8-f7d9-4cd1-ac06-3ecdd2127242.png align="center")

let's see the breakdown of code, like what is actually happening here:

1. **initialization:** In the `main` function, we begin by printing a welcome message to the console using `print("Welcome to Flutter Series")`.
    
2. **Class Creation:** we created an instance of the `myClass` class by declaring `var myC = myClass();`. This instance will allow us to access the methods defined within the class.
    
3. **Method Call - First:** Here we're calling the `Add` method of the `myClass` class with the arguments `5` and `6` using `myC.Add(5, 6)`. This method is responsible for adding the two numbers.
    
4. **Method Execution - First:** Inside the `Add` method, the parameters `no1` and `no2` are initialized with the values `5` and `6`. The method then calculates the sum of these two numbers and stores it in a variable `sum`. The `return` statement sends this result back to the point of the method call.
    
5. **Printing the First Result:** The result of the first method call, which is the sum of 5 and 6, is printed to the console using `print(myC.Add(5, 6))`.
    
6. **Method Call - Second:** Here now, we are calling the `Add` method again, but this time with the arguments `200` and `300` using `myC.Add(200, 300)`.
    
7. **Method Execution - Second:** The `Add` method is executed again, this time with the parameters `no1` set to 200 and `no2` set to 300. It calculates the sum and returns it.
    
8. **Printing the Second Result:** The result of the second method call, which is the sum of 200 and 300, is printed to the console using `print(myC.Add(200, 300))`.
    

So this is how this program is working, I hope now you're able to understand this code in more depth and clarity.

> In the next upcoming blogs, I'm going to cover all the basics of Dart like List in Dart and all.

---

## **Ending Note**

So, That's all about Basics of ***Dart Language (part 1)***, hope this blog feels helpful to you & I'll cover other topics regarding Flutter in my upcoming blogs.

You can ask your doubts and submit your feedback in the comment section below and connect with me on my socials: [**LinkedIn**](https://www.linkedin.com/in/maharshi-sinha-78b1001b7/) / [**Twitter(X)**](https://twitter.com/sinha_maharshi) to let me know what you think of it. Stay tuned for some more interesting blogs coming up soon in this series.

Also, If you like my content and want to " [**support**](https://www.buymeacoffee.com/maharshisinha) " my efforts please like👍🏻, share🔃 & subscribe to the newsletter 📩 to be notified whenever I post a new blog.

Happy Fluttering! Have a nice day :)