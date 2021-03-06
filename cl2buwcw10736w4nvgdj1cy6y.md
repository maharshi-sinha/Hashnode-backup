## JavaScript Beginner to advance all basic concepts!

Hey folks ! Welcome again in my new blog & in this blog I'm gonna cover **almost everything** about * **JavaScript** * so, If you're having zero knowledge of Js then also you are most welcome. Here I'll try to cover every point that's necessary to know about JavaScript for fresher.
_____________________________________________________________________________________________________________

# What is Java Script ?

So, JavaScript is a *lightweight, cross-platform, and interpreted scripting language*. It is well-known for the development of **web pages**, many non-browser environments also use it. JavaScript can be used for `Client-side developments` as well as `Server-side developments`

- ##  Basic intro and starting :

βͺ Used to make web pages Interactive.<br>
βͺ File Extension: `file_name.js`


- 
## How to link with HTML :
#### πThere are 2 ways to link a js file with an HTML file :-
1. "External JS"
2. "Internal JS" using the **< script >** tag<br>


- 
 ##  Variable :
π΄ Container used to store data (of different types).
 #### π 3 ways to create it


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

π΄ " Type of a particular data is called *data types* "
#### π There are 7 data-types in *Js*

-  >**String**  β‘  var a = "Hashnode";
-  >**Number**  β‘  var a = 5;
-  >**Boolean**  β‘  var a = True/False;
-  >**Array**  β‘  var a = [1, "a", true];
-  >**Object**  β‘  var a = {prop: "val"};
-  >**Null**  β‘  var a = null;
-  >**Undefined**  β‘  var a;

- 
##  Operators :

π΄ " Symbols to perform operation on data "
#### πThere are 4 operator types in *JS*

-  >**Arithmetic** Operators (+,-,*,/,%)
-  >**Assignment** Operators (=, +=,......)
-  >**Comparison** Operators (>, <, ==, ......)
-  >**Logical** Operators (&&, ||, !)

π Example :-


```javascript
var a = 10;
var b = 20;
var c = a+b;
``` 

- 
 ##  Comments :

π΄ " Statements that are not executed while execution "
#### πThere are 2 to write them in *JS* :


1.  **Single Line Comment**
> //single line
2. ** Multi Line Comment**
> /** * ** multi line comment ** * **/

- 
 ##  Print or Write :

π΄ " Printing or Writing something on a screen. "
#### πThere are 2 ways to print/write in *JS* :



- βπΌ On Browser Console

```javascript
console.log("anything");
``` 


- βπΌ On document/screen

```javascript
document.write("anything");
``` 

- 
 ##  Functions :

π΄ " Block of code that perform a specific task "
#### πThere are 2 to write them in *JS* :


π© Regular Function

```javascript
let name = function( parameters )
{//code}
``` 

π© Arrow Function

```js
let name = ( parameters ) =>
{//code}
``` 

- 
 ##  Loops :

π΄ " Used for repeated execution of code until a certain condition "
#### πThere are 3 types of Loops in *JS* :


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

π΄ " Collection of data stored under the same name. "
#### πData could be of any type 
#### Syntax :


```js
let arrayName = [ item0, item1,....... ];
``` 
` note : Location of an item in an array is called Index of an Array`
`Array always starts from 0th Index`

#### π Multi-Dimensional Array :
βͺ " Array within an array" 

- 
 ##  Objects :

π΄ " Collection of data store in form of name/value pairs. "
#### πSyntax :

```js
 let objectName = { name : "value" };
``` 
` Here, name = property & value = Value`

- 
 ##  If-Else :

π΄ " Executes the code if the condition is true, else another code. "
#### πSyntax :

```js
if ( condition == true ) {
// execute this code
} else {
// execute this code
}
``` 
- 
 ##  Switch-Case Statement :

π΄ " It has 1 expression and some cases. Cases compare with expression. "
#### πSyntax :

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

π΄ " New way to write strings using back-ticks ( *`* *`* ). "
#### πSyntax :

```js
let str = `Hello`;
``` 

#### πEasy Interpolation :
( insertion of variables in the string ).

```js
let name = "Hashnode";
let str = `Hello ${ name }` ;
// Output : Hello Hashnode
``` 


- 
 ##  Jump Statements :

π΄ " Statements to transfer the control from one place to another. "
#### πreturn value ;
βͺreturn value to the calling code.
#### πbreak ;
βͺstops the execution.
#### πcontinue ;
βͺcontrol jumps to beginning of loop

- 
 ##   Events :
π΄ " Action occurs when user interact with the web page. "
#### πExample : Button clicked
#### πSyntax :

```js
< element onevent = 'some Javascript'>
``` 
` Here, "oneventname " eg. onclick`<br>
` and "some Javascript" -> js code to be execute`

- 
 ##   this Keyword :
π΄ " `this` is a pre-defined words that always points to Js object. "<br>
βͺ **Globally**, it represents the `window object`.<br>
βͺ**In-object method**, it represents the `object`.<br>
βͺ**In function**, it represents the `window object`.<br>

- 
 ##   DOM :
π΄**"Document Object Model"**<br>
π It looks like a Tree<br>
πTree of all HTML elements <br>
πEverything (element, text, attribute) is called **Node.**

![DOM.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1650569699827/v4kGUx7EC.jpg)

- 
 ##   DOM Methods :
π΄ " These are the methods to access the DOM node or element. "

```js
document.method();
```
π `.getElementByld`<br>
π` .getElementsByTagName` <br>
π`.querySelector`

- 
 ##   BOM :

π΄**"Browser Object Model"**<br>
πIt also looks like a Tree <br>
πTree of all browser objects<br>
πThis include the info about the browser.


![html-dom.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1650570127874/nSTdsVXhw.jpg)
- 
 ##   BOM  Methods :
π΄ " These are the methods to access the BOM node or element. "

```js
window.method()
```
π`.open()`<br>
π`.resizeTo()`<br>
π`.close()`

- 
 ##   Closures :
π΄ " Feature in JS where inner function has access to outer function's variables. "

#### π Example :

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
π΄ " Allow you to split code into separate files. "

π© Modules rely on import and export statements. <br>
π© Send data using export and get data using import.

```js
export const name = "Maharshi";
```
```js
import {name,age} from "./file.js";
```

- 
 ##   CallBacks() :
π΄ " function passed to another function as an argument. "

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
π΄ " It is an object that links the producing code and consuming code. "

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
π΄ " Awaits makes the function wait for a promise. "
```js
let value = await promise; 
```
βͺ await simply puts the statement on `wait`

- 
 ##   Strict Mode :
π΄ " makes your js coding environment strict. "

#### π Syntax : 
```js 
"use strict"; 
```
#### π *Code will be executed in strict mode*.
#### π *No undeclare variables can be used*.
#### π *Makes you code more accurate.*

- 
 ##   Async :
π΄ " async is just a simple function returning a promise. "
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

**π² Js Stopwatch**<br>
**π² To-do List**<br>
**π² Weather app**<br>
**π² Tic Tac Toe app**<br>
**π² Music Player**

_____________________________________________________________________________________________________________
So, That's all about JavaScript.

Reach me out in the comments below or in my socials : [LinkdIn](https://www.linkedin.com/in/maharshi-sinha-78b1001b7) / [Twitter](https://twitter.com/sinha_maharshi?s=09) to let me know what you think of it.
Stay tuned for some more interesting blogs coming up soon.

Also, If you like my content and want to support my efforts please likeππ», shareπ & subscribe to the newsletter π© to be get **notified** whenever I post a new blog. 

Happy Coding ! <br>
Have a nice day :)