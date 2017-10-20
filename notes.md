## Definitions

* **Syntax Parser**: a program that reads your code and determine what it does and if its grammar is valid (Javascript Engine)


* **Lexical Environment**: where something sits physically in the code you write

* **Execution Context**: a wrapper to help manage the code that is running. It has a *create fase* where all of the objects are created stored in memory (hoisting) and a *running fase* where the code is executed
  * Global Execution Context: the root context. It has the global window object *this*
  * An execution context is created for each function
  
* **Execution Stack**: is the way the execution contexts are created and run, the Global Execution Context is on top of them. For each function there is a new *execution context* and *variable environment*


* **Hoisting**: setup memory space for variables and functions. Variables setup (and set equal to undefined)


* **Single Threaded**: one command at a time


* **Synchronous**: one at a time


* **Invocation**: running a function


* **Variable Environment**: where the variable live and how they relate to each other in memory


* **Outer Environment**: Each execution context has a reference to its outer environment, and it depends where it sits *lexically* and *physically*


* **Scope Chain**: It's the order in which the Javascript engine looks for the outer environment reference, it depends on where each function sits lexically. It tells where to find a variable or object depending on it's outer environment, so it start looking for it all they way up until it finds it. Another way to look at it is asking *Who created me?*

   ```javascript
   function a() {
        function b() {
            console.log(myvar);            
       }
       var myVar = 2;
       b();
   }
   var myVar = 1;
   a();
   
   OUTPUT: 2
   
   ```
   
   ```javascript
   function a() {
       var myVar = 2;
       b();
   }
   function b() {
        console.log(myvar);            
   }
   var myVar = 1;
   a();
   
   OUTPUT: 1
   
   ```




