---
title: JavaScript Questions
layout: layouts/page.njk
permalink: /questions/javascript-questions/index.html
---

* **Explain event delegation.**
  
  >Attaching event listeners to parent node, instead of every child, present or newly created, is event delegation. It makes use of event bubbling, where the event on a child bubbles up to the parent. So instead of adding an event listener to a child, and adding one every time a new child is added, we add the listener on parent. Following is a basic example taken from David Walsh’s blog([here](https://davidwalsh.name/event-delegate)).

* **Explain how `this` works in JavaScript.**
  >All functions in JavaScript have properties, just as objects have properties. And when a function executes, it gets the this property — a variable with the value of the object that invokes the function where this is used. The this reference ALWAYS refers to (and holds the value of) an object — a singular object — and it is usually used inside a function or a method, although it can be used outside a function in the global scope. Note that when we use strict mode, this holds the value of undefined in global functions and in anonymous functions that are not bound to any object. A good resource to understand this is [here](http://javascriptissexy.com/understand-javascripts-this-with-clarity-and-master-it) and [MDN](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Operators/thishttps://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Operators/this).

  * **Can you give an example of one of the ways that working with `this` has changed in ES6?**

* **Explain how prototypal inheritance works.**
  >JavaScript only has one construct: objects. Each object has an internal link to another object called its prototype. That prototype object has a prototype of its own, and so on until an object is reached with null as its prototype. null, by definition, has no prototype, and acts as the final link in this prototype chain. For better understanding please refer to [this](http://javascriptissexy.com/javascript-prototype-in-plain-detailed-language), [this](http://yehudakatz.com/2011/08/12/understanding-prototypes-in-javascript) and [this](https://developer.mozilla.org/en/docs/Web/JavaScript/Inheritance_and_the_prototype_chain) as a resource.

* **What's the difference between a variable that is: `null`, `undefined` or undeclared?**
  >Undeclared is any variable that has not been declared yet. Console throws an error for this. Undefined is a declared variable that has no assigned value, yet. Null is a value that has been assigned to a variable. Read more about them [here](http://lucybain.com/blog/2014/null-undefined-undeclared).
  ```
  Null !== NULL !== null in javascript. 
  Also, null == undefined // true
  null === undefined //false
  null === null //true
  ```

  * **How would you go about checking for any of these states?**

* **What is a closure, and how/why would you use one?**
  >A closure is an inner function that has access to the outer (enclosing) function’s variables — scope chain. The closure has three scope chains: it has access to its own scope (variables defined between its curly brackets), it has access to the outer function’s variables, and it has access to the global variables. Read [here](http://javascriptissexy.com/understand-javascript-closures-with-ease) and at [MDN](https://developer.mozilla.org/en/docs/Web/JavaScript/Closures). You use one when you later need access to the variables of a function that has returned already.

* **What language constructions do you use for iterating over object properties and array items?**

* **Can you describe the main difference between the `Array.forEach()` loop and `Array.map()` methods and why you would pick one versus the other?**

* **What's a typical use case for anonymous functions?**
  >Anonymous functions are function expressions, and thus we can pass them as variables and return functions. When used as IIFE, they are used to maintain scope. [This](http://stackoverflow.com/questions/12930272/javascript-closures-vs-anonymous-functions) is a very good resource to understand how closures and anonymous functions work.

* **What's the difference between host objects and native objects?**
  >Host — objects provided by environment like window, document by browser. Native — object in an ECMAScript implementation whose semantics are fully defined by this specification rather than by the host environment. Eg. Array, String etc. Read more [here](http://es5.github.io/#x4.3.6).

* **Explain the difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?**

* **Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`**

* **Can you explain what `Function.call` and `Function.apply` do? What's the notable difference between the two?**
  >First one is a function declaration. the second one returns the return value of function Person and assigns it to person variable. The third creates a new instance of an object based on the Person function. So the variable (person) is now an Object. For more detailed discussion refer to [this](http://lucybain.com/blog/2015/js-new-keyword-and-functions) article.

* **Explain `Function.prototype.bind`.**
  >Function.prototype.bind is used to set this explicitly. It returns a function with given this context that can be called later. Read [this](http://javascriptissexy.com/javascript-apply-call-and-bind-methods-are-essential-for-javascript-professionals), [this](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_objects/Function/bind) and [this](https://www.smashingmagazine.com/2014/01/understanding-javascript-function-prototype-bind) article for further understanding.

* **What's the difference between feature detection, feature inference, and using the UA string?**
  >Feature Detection — When you check if a certain feature exists. Feature Inference — checks for a feature just like feature detection, but uses another function because it assumes it will also exist. Assumptions are bad bad bad. UA String — UA String or User Agent String is a string text of data that each browsers send and can be accessed with navigator.userAgent. Checking the [UA string](https://developer.mozilla.org/en-US/docs/Browser_detection_using_the_user_agent) is an old practice and should not be used anymore. Read [here](http://stackoverflow.com/questions/20104930/whats-the-difference-between-feature-detection-feature-inference-and-using-th) for detailed discussion.

* **Explain "hoisting".**
  >Variable declarations (and declarations in general) are processed before any code is executed, declaring a variable anywhere in the code is equivalent to declaring it at the top. This also means that a variable can appear to be used before it’s declared. This behavior is called “hoisting”, as it appears that the variable declaration is moved to the top of the function or global code. Read more [here](http://javascriptissexy.com/javascript-variable-scope-and-hoisting-explained), [here](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Statements/var) and [here](http://www.adequatelygood.com/JavaScript-Scoping-and-Hoisting.html). It’s a tricky concept and should be understood well.

* **Describe event bubbling.**
  >[This](http://stackoverflow.com/questions/4616694/what-is-event-bubbling-and-capturing) article is a very good resource to understand event bubbling and capturing in detail. Event bubbling and capturing are two ways of event propagation in the HTML DOM API, when an event occurs in an element inside another element, and both elements have registered a handle for that event. The event propagation mode determines in [which order the elements receive the event](http://www.quirksmode.org/js/events_order.html). With bubbling, the event is first captured and handled by the innermost element and then propagated to outer elements. With capturing, the event is first captured by the outermost element and propagated to the inner elements.

* **Describe event capturing.**

* **What's the difference between an "attribute" and a "property"?**
  >Attributes are defined by HTML. Properties are defined by DOM. Some HTML attributes have 1:1 mapping onto properties. id is one example of such. Some do not (e.g. the value attribute specifies the initial value of an input, but the valueproperty specifies the current value). Read further [here](http://lucybain.com/blog/2014/attribute-vs-property) and [here](http://stackoverflow.com/questions/6003819/properties-and-attributes-in-html).

* **What are the pros and cons of extending built-in JavaScript objects?**

* **What is the difference between `==` and `===`?**
  >The identity (===) operator behaves identically to the equality (==) operator except no type conversion is done, and the types must be the same to be considered equal. Read detailed answer [here](http://stackoverflow.com/questions/359494/does-it-matter-which-equals-operator-vs-i-use-in-javascript-comparisons).

* **Explain the same-origin policy with regards to JavaScript.**
  >The same origin policy states that a web browser permits script contained in one page (or frame) to access data in another page (or frame) only if both the pages have the same origin. It is a critical security mechanism for isolating potentially malicious documents. Two pages have the same origin if the protocol, port (if one is specified), and host are the same for both pages. Read details [here](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy) and [here](https://www.w3.org/Security/wiki/Same_Origin_Policy).

* **Why is it called a Ternary operator, what does the word "Ternary" indicate?**
  >“Ternary” means operands with three(n-ary) param. This is a one-line shorthand for an if-then statement. It is called a ternary operator or a conditional operator. Read [this](http://lucybain.com/blog/2014/js-ternary) for example.

* **What is strict mode? What are some of the advantages/disadvantages of using it?**
  >Strict mode is a way to opt in to a restricted variant of JavaScript. Strict mode isn’t just a subset: it intentionally has different semantics from normal code. Browsers not supporting strict mode will run strict mode code with different behavior from browsers that do, so don’t rely on strict mode. Read [here](http://ejohn.org/blog/ecmascript-5-strict-mode-json-and-more), [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode) and [here](http://lucybain.com/blog/2014/js-use-strict).

* **What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?**
  >Example: CoffeeScript. Pros/Cons: Syntactic sugar, readable code, and use of good patterns vs debugging and compilation issues. [Read](http://programmers.stackexchange.com/questions/72569/what-are-the-pros-and-cons-of-coffeescript) this answer for details.

* **What tools and techniques do you use debugging JavaScript code?**
  >Web/Browser console using console.log. Firebug, Developer Tools, stop points. Read [this](http://stackoverflow.com/questions/988363/how-can-i-debug-my-javascript-code), [this](https://developer.mozilla.org/en-US/docs/Mozilla/Debugging/Debugging_JavaScript) and [this](https://developer.chrome.com/devtools/docs/javascript-debugging) article for help.

* **Explain the difference between mutable and immutable objects.**
  * **What is an example of an immutable object in JavaScript?**
  * **What are the pros and cons of immutability?**
  * **How can you achieve immutability in your own code?**
  >Mutable objects are those whose state is allowed to change over time. An immutable value is the exact opposite — after it has been created, it can never change. Strings and Numbers are inherently immutable in javascript. Refer [this article](http://www.sitepoint.com/immutability-javascript) for further answers.

* **Explain the difference between synchronous and asynchronous functions.**
  >Synchronous: Step wise execution. Next line executed after first. Asynchronous: Execution moves to next step before first is finished. Read [this](http://stackoverflow.com/questions/748175/asynchronous-vs-synchronous-execution-what-does-it-really-mean) article for further explanation.

* **What is event loop?**
  * **What is the difference between call stack and task queue?**
  >JavaScript has a concurrency model based on an “event loop”. Read this article by [MDN](https://developer.mozilla.org/en/docs/Web/JavaScript/EventLoop), [this](http://stackoverflow.com/questions/15093838/is-there-a-difference-between-event-loop-and-task-queue-in-browsers) and [this](http://blog.carbonfive.com/2013/10/27/the-javascript-event-loop-explained) one for details and explanation.

* **What are the differences between variables created using `let`, `var` or `const`?**

* **What are the differences between ES6 class and ES5 function constructors?**

* **Can you offer a use case for the new arrow `=>` function syntax? How does this new syntax differ from other functions?**

* **What advantage is there for using the arrow syntax for a method in a constructor?**

* **What is the definition of a higher-order function?**

* **Can you give an example for destructuring an object or an array?**

* **Can you give an example of generating a string with ES6 Template Literals?**

* **Can you give an example of a curry function and why this syntax offers an advantage?**

* **What are the benefits of using `spread syntax` and how is it different from `rest syntax`?**

* **How can you share code between files?**

* **Why you might want to create static class members?**

## Coding questions
* **Make this work:**
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```
```javascript
Array.prototype.duplicator=function() {
  return this.concat(this);
}
```

* **Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`**


# **Credit**:
[neha nupoor](https://medium.com/@nupoor_neha/javascript-front-end-interview-questions-1cbc5e32792b)