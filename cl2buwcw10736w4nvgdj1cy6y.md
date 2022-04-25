## Javascript Beginner to advance all basic concepts!

Hey folks ! Welcome again in my new blog & in this blog I'm gonna cover **almost everything** about * **JavaScript** * so, If you're having zero knowledge of Js then also you are most welcome. Here I'll try to cover every point that's necessary to know about JavaScript for fresher.
_____________________________________________________________________________________________________________

# What is Java Script ?

So, JavaScript is a *lightweight, cross-platform, and interpreted scripting language*. It is well-known for the development of **web pages**, many non-browser environments also use it. JavaScript can be used for `Client-side developments` as well as `Server-side developments`

- ##  Basic intro and starting :

↪ Used to make web pages Interactive.<br>
↪ File Extension: `file_name.js`


- 
## How to link with HTML :
#### 🌟There are 2 ways to link a js file with an HTML file :-
1. "External JS"
2. "Internal JS" using the **< script >** tag<br>


- 
 ##  Variable :
🔴 Container used to store data (of different types).
 #### 🌟 3 ways to create it


-  >With var keyboard

``` javascript
var name = data-of-any-data-type;
``` 

- >With let Keyboard 
 

```javascript
let name = data-of-any-data-type;
``` 


- >With  const keyword

```javascript
const name = data-of-any-data-type;
``` 
- 
 ##  Data Types :

🔴 " Type of a particular data is called *data types* "
#### 🌟 There are 7 data-types in *Js*

-  >**String**  ➡  var a = "Hashnode";
-  >**Number**  ➡  var a = 5;
-  >**Boolean**  ➡  var a = True/False;
-  >**Array**  ➡  var a = [1, "a", true];
-  >**Object**  ➡  var a = {prop: "val"};
-  >**Null**  ➡  var a = null;
-  >**Undefined**  ➡  var a;

- 
##  Operators :

🔴 " Symbols to perform operation on data "
#### 🌟There are 4 operator types in *JS*

-  >**Arithmetic** Operators (+,-,*,/,%)
-  >**Assignment** Operators (=, +=,......)
-  >**Comparison** Operators (>, <, ==, ......)
-  >**Logical** Operators (&&, ||, !)

🚀 Example :-


```javascript
var a = 10;
var b = 20;
var c = a+b;
``` 

- 
 ##  Comments :

🔴 " Statements that are not executed while execution "
#### 🌟There are 2 to write them in *JS* :


1.  **Single Line Comment**
> //single line
2. ** Multi Line Comment**
> /** * ** multi line comment ** * **/

- 
 ##  Print or Write :

🔴 " Printing or Writing something on a screen. "
#### 🌟There are 2 ways to print/write in *JS* :



- ☝🏼 On Browser Console

```javascript
console.log("anything");
``` 


- ✌🏼 On document/screen

```javascript
document.write("anything");
``` 

- 
 ##  Functions :

🔴 " Block of code that perform a specific task "
#### 🌟There are 2 to write them in *JS* :


🟩 Regular Function

```javascript
let name = function( parameters )
{//code}
``` 

🟩 Arrow Function

```js
let name = ( parameters ) =>
{//code}
``` 

- 
 ##  Loops :

🔴 " Used for repeated execution of code until a certain condition "
#### 🌟There are 3 types of Loops in *JS* :


1.  For Loop
1. While Loop
1. Do-While Loop

Example :- 

```js
# For Loop
for( init; condition; var++/--)
__________________________________
# While Loop
while ( condition ){ }
__________________________________
# Do-While Loop
do { code } while ( condition )
``` 

- 
 ##  Arrays :

🔴 " Collection of data stored under the same name. "
#### 🌟Data could be of any type 
#### Syntax :


```js
let arrayName = [ item0, item1,....... ];
``` 
` note : Location of an item in an array is called Index of an Array`
`Array always starts from 0th Index`

#### 🌟 Multi-Dimensional Array :
↪ " Array within an array" 

- 
 ##  Objects :

🔴 " Collection of data store in form of name/value pairs. "
#### 🌟Syntax :

```js
 let objectName = { name : "value" };
``` 
` Here, name = property & value = Value`

- 
 ##  If-Else :

🔴 " Executes the code if the condition is true, else another code. "
#### 🌟Syntax :

```js
if ( condition == true ) {
// execute this code
} else {
// execute this code
}
``` 
- 
 ##  Switch-Case Statement :

🔴 " It has 1 expression and some cases. Cases compare with expression. "
#### 🌟Syntax :

```js
switch ( expression ) {
case a :
// code
     break;
case b:
// code
    break;
  default:  
// code
} 
``` 
- 
 ##  Template Strings :

🔴 " New way to write strings using back-ticks ( *`* *`* ). "
#### 🌟Syntax :

```js
let str = `Hello`;
``` 

#### 🌟Easy Interpolation :
( insertion of variables in the string ).

```js
let name = "Hashnode";
let str = `Hello ${ name }` ;
// Output : Hello Hashnode
``` 


- 
 ##  Jump Statements :

🔴 " Statements to transfer the control from one place to another. "
#### 🌟return value ;
↪return value to the calling code.
#### 🌟break ;
↪stops the execution.
#### 🌟continue ;
↪control jumps to beginning of loop

- 
 ##   Events :
🔴 " Action occurs when user interact with the web page. "
#### 🌟Example : Button clicked
#### 🌟Syntax :

```js
< element onevent = 'some Javascript'>
``` 
` Here, "oneventname " eg. onclick`<br>
` and "some Javascript" -> js code to be execute`

- 
 ##   this Keyword :
🔴 " `this` is a pre-defined words that always points to Js object. "<br>
↪ **Globally**, it represents the `window object`.<br>
↪**In-object method**, it represents the `object`.<br>
↪**In function**, it represents the `window object`.<br>

- 
 ##   DOM :
🔴**"Document Object Model"**<br>
🌟 It looks like a Tree<br>
🌟Tree of all HTML elements <br>
🌟Everything (element, text, attribute) is called **Node.**

![DOM.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1650569699827/v4kGUx7EC.jpg)

- 
 ##   DOM Methods :
🔴 " These are the methods to access the DOM node or element. "

```js
document.method();
```
🌟 `.getElementByld`<br>
🌟` .getElementsByTagName` <br>
🌟`.querySelector`

- 
 ##   BOM :

🔴**"Browser Object Model"**<br>
🌟It also looks like a Tree <br>
🌟Tree of all browser objects<br>
🌟This include the info about the browser.


![html-dom.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1650570127874/nSTdsVXhw.jpg)
- 
 ##   BOM  Methods :
🔴 " These are the methods to access the BOM node or element. "

```js
window.method()
```
🌟`.open()`<br>
🌟`.resizeTo()`<br>
🌟`.close()`

- 
 ##   Closures :
🔴 " Feature in JS where inner function has access to outer function's variables. "

#### 🚀 Example :

```js
function hello(){
var a = 10;
var b = 20;
function print(){
var c = a+b;
console.log(c);
}
print();
}
hello();
```

- 
 ##   Modules :
🔴 " Allow you to split code into separate files. "

🟩 Modules rely on import and export statements. <br>
🟩 Send data using export and get data using import.

```js
export const name = "Maharshi";
```
```js
import {name,age} from "./file.js";
```

- 
 ##   CallBacks() :
🔴 " function passed to another function as an argument. "

```js
function print1(callback){
     console.log("hello");
     callback();
}
function print2(){
     console.log("world");
}
print1(print2);
```

- 
 ##   Promises :
🔴 " It is an object that links the producing code and consuming code. "

```js
let myPromise = new
promise( function(myResolve, myReject){
// producing code

    myResolve(); //Successful
    myReject();  //error
});

// Consuming Code

    myPromise.then(
            function(value) { /* code if successful */},
            function(error) { /* code if some error */}
);
```

- 
 ##   Await :
🔴 " Awaits makes the function wait for a promise. "
```js
let value = await promise; 
```
↪ await simply puts the statement on `wait`

- 
 ##   Strict Mode :
🔴 " makes your js coding environment strict. "

#### 🌟 Syntax : 
```js 
"use strict"; 
```
#### 🚀 *Code will be executed in strict mode*.
#### 🚀 *No undeclare variables can be used*.
#### 🚀 *Makes you code more accurate.*

- 
 ##   Async :
🔴 " async is just a simple function returning a promise. "
```js
async function mf(){
    return "Hello";
}
```
in same as :

  ```js
 function mf(){
    return promise.resolve("Hello");
  }
  ```
- 
 ##   JS Projects for Begineer :

**💲 Js Stopwatch**<br>
**💲 To-do List**<br>
**💲 Weather app**<br>
**💲 Tic Tac Toe app**<br>
**💲 Music Player**

_____________________________________________________________________________________________________________
So, That's all about JavaScript.

Reach me out in the comments below or in my socials : [LinkdIn](https://www.linkedin.com/in/maharshi-sinha-78b1001b7) / [Twitter](https://twitter.com/sinha_maharshi?s=09) to let me know what you think of it.
Stay tuned for some more interesting blogs coming up soon.

Also, If you like my content and want to support my efforts please like👍🏻, share🔃 & subscribe to the newsletter 📩 to be get **notified** whenever I post a new blog. 

Happy Coding ! <br>
Have a nice day :)