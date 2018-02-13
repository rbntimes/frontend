# Notes

## Notes week-1
-
## Notes week-2

### Chapter 1: What is scope

#### Compiler theory

> The ability to store values and pull values out of variables is what gives a program _state_.

In a traditional compiled-language process, a chunk of source code, your program, will undergo typically three steps before it is executed, roughly called "compilation".

1.  **Tokenizing/Lexing**: breaking up a string of characters into meaningful chunks, called tokens
2.  **Parsing**: Taking a stream of tokens and turning it into a tree of nested elements
3. **Code-Generation**: The process of taking this tree and turning it into executable code

The Javascript engine is vastly more complex than just those three steps.

#### Understanding scope

##### The cast

1.  Engine: Responsible for start-to-finish compilation and execution of our Javascript program.
2.  Compiler: one of Engine's friends; handles all the dirty work of parsing and code-generation (see previous section).
3.  Scope: another friend of Engine; collects and maintains a look-up list of all the declared identifiers (variables), and enforces a strict set of rules as to how these are accessible to currently executing code.

** LHS **: Left-hand Side  
Finding the defined variable  
** RHS **: Right-hand Side  
The value of the variable

![Global scope](https://github.com/getify/You-Dont-Know-JS/raw/master/scope%20%26%20closures/fig1.png "Scope")
> **Global scope**

Javascript will go from bottom to top like an elevator in this building looking for the variable you've asked for.

#### IIFE (Immediately Invoked Function Expression)

> IIFE is a JavaScript function that runs as soon as it is defined.

```
(function () {
    var aName = "Barry";
})();
// Variable name is not accessible from the outside scope
aName // throws "Uncaught ReferenceError: aName is not defined"
```
[Source](https://developer.mozilla.org/en-US/docs/Glossary/IIFE)

Can be useful when not wanting a variable injected into the global scope. 
