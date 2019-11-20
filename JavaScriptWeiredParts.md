# JavaScript Weired Parts

###  Context and Environment

- **Lexical Environment** is the environment of the function where it is written. That is, the static order/place where it is situated, regardless from where it is called from.

- **Scope** of a variable/function is basically the locations from where a variable is visible/accessible.

- **Execution** contex is the status of the execution stack at any point during runtime. That is the current execution context.
A wrapper to help manage the running code. There are lots of lexical environments. Which one is currently running is managed by execution context. 

###  Name/Value Pairs and objects

**Object** is a collection of name/value pairs.

eg: Address="100 King Street"

### Global env and global object
Execution Context creates 2 things: global object and `this`.
Browser: `this`->window object(which is a global object)
NodeJs: `this`-> current module.export object   `global`-> window object

### Execution context create and hoisting
Execution context will set up the memory space for the functions and variables that going to be used in a limited way. 
It will place entire function(the name and the code inside) to the memory space, but put a placeholder `undefined` to variable. The assignment to variable will happen during execution. 
```
b()
console.log(a)

let a = "happy"
function b (){
console.log("func b is called")
}
```
output:
```
$ "func b is called"
$ undefined
```
