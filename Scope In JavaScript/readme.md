# Understanding the Magic of Lexical Environments in JavaScript

## A lexical environment consists of Environment Record and a reference to the outer environment

<br>
A lexical environment is a fundamental concept in programming that refers to the set of variables, functions, and objects that are available for use at a particular point in your code. Every time you run a piece of code, a new lexical environment is created to store the relevant information.

<br>
The lexical environment is created at the time of execution and is based on the scope in which the code is executed. There are two main types of lexical environments: global and local.

<br>

## Global Lexical Environment
A global lexical environment is created when your code starts running, and it consists of all the variables, functions, and objects that are defined in the global scope. The global scope refers to any code that is outside of a function or block statement.

Here's an example of a global lexical environment:

```js
// javascript code Global scope

const firstName = "Shrish";

function sayHello() {
  console.log(`Hello ${firstName}`);
}

sayHello(); // Output: Hello Shrish
```
In this example, the global lexical environment contains the firstname variable and the sayHello() function. When the sayHello() function is called, it looks for the firstName variable in its current lexical environment (the global environment) and finds it there.

<br>

## Local Lexical Environment
A local lexical environment, on the other hand, is created every time a new function is called. It contains all the variables, functions, and objects that are defined within the function and its parent scopes.

Here's an example of a local lexical environment:
```js

// javascript code Global scope
const firstName = "Shrish";

function sayHello() {
  // Local scope
  const lastName = "Kerur";
  console.log(`Hello ${firstName} ${lastName}`);
}

sayHello(); // Output: Hello Shrish Kerur
```

In this example, the local lexical environment is created when the sayHello() function is called. It contains the lastName variable, which is defined in the function's local scope, as well as the firstName variable, which is defined in the global scope.

<br>

## Nested Lexical Environments
There are also nested lexical environments, which occur when a function is defined within another function. In this case, the inner function has access to all the variables, functions, and objects defined in its own lexical environment, as well as those defined in the parent environment.

Here's an example of a nested lexical environment:


```js
// javascript code Global scope
const firstName = "Shrish";

function sayHello() {
  // Local scope 1
  const lastName = "Kerur";

  function greet() {
    // Local scope 2
    const title = "Mr.";
    console.log(`Hello ${title} ${firstName} ${lastName}`);
  }

  greet();
}

sayHello(); // Output: Hello Mr. Shrish Kerur
```

In this example, the greet() function is defined within the sayHello() function, creating a nested lexical environment. The greet() function has access to the title variable, which is defined in its own lexical environment, as well as the firstName and lastName variables, which are defined in the parent lexical environments.

<br>

## Conclusion
In summary, a lexical environment is a set of variables, functions, and objects that are available for use at a particular point in your code.

There are two main types of lexical environments: <b>Global</b> and <b>Lexical</b>.

The global environment contains all the variables, functions, and objects that are defined in the global scope, while a local environment is created every time a new function is called and contains all the variables, functions, and objects defined within that function and its parent scopes.

<br>
Nested lexical environments occur when a function is defined within another function and give the inner function access to variables, functions, and objects defined in the parent environment.
