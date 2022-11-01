1. Explain event delegation
   <details>
   <summary title = "Answer"><span>Answer</span></summary>
   <code>
   <p>
   Event delegation is a technique involving adding event listeners to a parent element instead of adding them to the descendant elements. The listener will fire whenever the event is triggered on the descendant elements due to event bubbling up the DOM. The benefits of this technique are:

   Memory footprint goes down because only one single handler is needed on the parent element, rather than having to attach event handlers on each descendant.
   There is no need to unbind the handler from elements that are removed and to bind the event for new elements.

   References:<p>
   <a href="https://davidwalsh.name/event-delegate" target="_blank" rel="noopener noreferrer">
   https://davidwalsh.name/event-delegate
   </a>
   <br>
   <a href="https://stackoverflow.com/questions/1687296/what-is-dom-event-delegation" target="_blank" rel="noopener noreferrer">
   https://stackoverflow.com/questions/1687296/what-is-dom-event-delegation
   </a>
   </code>
   </details>
   <hr>
   <br>

2. Explain how <code><i>this</i></code> works in JavaScript
   <details>
   <summary title = "Answer"><span>Answer</span></summary>
   <code>
   <p>
   There's no simple explanation for this; it is one of the most confusing concepts in JavaScript. A hand-wavey explanation is that the value of this depends on how the function is called. I have read many explanations on this online, and I found Arnav Aggrawal's explanation to be the clearest. The following rules are applied:

   1. If the new keyword is used when calling the function, this inside the function is a brand new object.
   2. If apply, call, or bind are used to call/create a function, this inside the function is the object that is passed in as the argument.
   3. If a function is called as a method, such as obj.method() — this is the object that the function is a property of.
   4. If a function is invoked as a free function invocation, meaning it was invoked without any of the conditions present above, this is the global object. In a browser, it is the window object. If in strict mode ('use strict'), this will be undefined instead of the global object.
   5. If multiple of the above rules apply, the rule that is higher wins and will set the this value.
   6. If the function is an ES2015 arrow function, it ignores all the rules above and receives the this value of its surrounding scope at the time it is created.
   </p>

   <p>
   For an in-depth explanation, do check out his article on <a href="https://codeburst.io/the-simple-rules-to-this-in-javascript-35d97f31bde3"  target="_blank" rel="noopener noreferrer">Medium</a>
   </p>
   </code>
   </details>
   <hr>
   <br>

3. Explain how prototypal inheritance works
   <details>
   <summary title = "Answer"><span>Answer</span></summary>
   </code>
   <p>
    This is an extremely common JavaScript interview question. All JavaScript objects have a __proto__ property with the exception of objects created with Object.create(null), that is a reference to another object, which is called the object's "prototype". When a property is accessed on an object and if the property is not found on that object, the JavaScript engine looks at the object's __proto__, and the __proto__'s __proto__ and so on, until it finds the property defined on one of the __proto__s or until it reaches the end of the prototype chain. This behavior simulates classical inheritance, but it is really more of <a href="https://davidwalsh.name/javascript-objects"   target="_blank" rel="noopener noreferrer">delegation than inheritance</a>.
    </code>

   <b>Example of Prototypal Inheritance:</b>
   <hr>
   </p>

   <b>
   <code>
   <p>
   function Parent() {
   this.name = 'Parent';
   }

   Parent.prototype.greet = function () {
   console.log('Hello from ' + this.name);
   };

   const child = Object.create(Parent.prototype);

   child.cry = function () {
   console.log('waaaaaahhhh!');
   };

   child.cry();
   // waaaaaahhhh!

   child.greet();
   // hello from Parent

   child.constructor;
   // ƒ Parent() {
   // this.name = 'Parent';
   // }

   child.constructor.name;
   // 'Parent'
   </p>
   </b>
   </code>
   </details>
   <hr>
   <br>

4. What do you think of AMD vs CommonJS?
   <details>
   <summary title = "Answer"><span>Answer</span></summary>
   <code>
   <p>

   </p>
   </code>
   </details>
   <hr>
   <br>

5. Explain why the following doesn't work as an IIFE: function foo(){ }();. What needs to be changed to properly make it an IIFE?
   <details>
   <summary title = "Answer"><span>Answer</span></summary>
   <code>
   <p>

   </p>
   </code>
   </details>
   <hr>
   <br>

6. What's the difference between a variable that is: null, undefined or undeclared? How would you go about checking for any of these states?
   <details>
   <summary title = "Answer"><span>Answer</span></summary>
   <code>
   <p>

   </p>
   </code>
   </details>
   <hr>
   <br>

7. What is a closure, and how/why would you use one?
   <details>
   <summary title = "Answer"><span>Answer</span></summary>
   <code>
   <p>

   </p>
   </code>
   </details>
   <hr>
   <br>

8. Can you describe the main difference between a .forEach loop and a .map() loop and why you would pick one versus the other?
   <details>
   <summary title = "Answer"><span>Answer</span></summary>
   <code>
   <p>

   </p>
   </code>
   </details>
   <hr>
   <br>

9. What's a typical use case for anonymous functions?
   <details>
   <summary title = "Answer"><span>Answer</span></summary>
   <code>
   <p>

   </p>
   </code>
   </details>
   <hr>
   <br>

10. How do you organize your code? (module pattern, classical inheritance?)
    <details>
    <summary title = "Answer"><span>Answer</span></summary>
    <code>
    <p>

   </p>
   </code>
   </details>
   <hr>
   <br>

11. What's the difference between host objects and native objects?
    <details>
    <summary title = "Answer"><span>Answer</span></summary>
    <code>
    <p>

   </p>
   </code>
   </details>
   <hr>
   <br>

12. Difference between: function Person(){}, var person = Person(), and var person = new Person()?
    <details>
    <summary title = "Answer"><span>Answer</span></summary>
    <code>
    <p>

   </p>
   </code>
   </details>
   <hr>
   <br>

13. What's the difference between .call and .apply?
    <details>
    <summary title = "Answer"><span>Answer</span></summary>
    <code>
    <p>

   </p>
   </code>
   </details>
   <hr>
   <br>

14. Explain Function.prototype.bind.
    <details>
    <summary title = "Answer"><span>Answer</span></summary>
    <code>
    <p>

   </p>
   </code>
   </details>
   <hr>
   <br>

15. When would you use document.write()?
    <details>
    <summary title = "Answer"><span>Answer</span></summary>
    <code>
    <p>

   </p>
   </code>
   </details>
   <hr>
   <br>

16. What's the difference between feature detection, feature inference, and using the UA string?
    Explain Ajax in as much detail as possible.
    What are the advantages and disadvantages of using Ajax?
    Explain how JSONP works (and how it's not really Ajax).
    Have you ever used JavaScript templating? If so, what libraries have you used?
    Explain "hoisting".
    Describe event bubbling.
    What's the difference between an "attribute" and a "property"?
    Why is extending built-in JavaScript objects not a good idea?
    Difference between document load event and document DOMContentLoaded event?
    What is the difference between == and ===?
    Explain the same-origin policy with regards to JavaScript.
    Make this work:
    Why is it called a Ternary expression, what does the word "Ternary" indicate?
    What is "use strict";? What are the advantages and disadvantages to using it?
    Create a for loop that iterates up to 100 while outputting "fizz" at multiples of 3, "buzz" at multiples of 5 and "fizzbuzz" at multiples of 3 and 5.
    Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
    Why would you use something like the load event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?
    Explain what a single page app is and how to make one SEO-friendly.
    What is the extent of your experience with Promises and/or their polyfills?
    What are the pros and cons of using Promises instead of callbacks?
    What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
    What tools and techniques do you use for debugging JavaScript code?
    What language constructions do you use for iterating over object properties and array items?
    Explain the difference between mutable and immutable objects.
    Explain the difference between synchronous and asynchronous functions.
    What is event loop? What is the difference between call stack and task queue?
    Explain the differences on the usage of foo between function foo() {} and var foo = function() {}
    What are the differences between variables created using let, var or const?
    What are the differences between ES6 class and ES5 function constructors?
    Can you offer a use case for the new arrow => function syntax? How does this new syntax differ from other functions?
    What advantage is there for using the arrow syntax for a method in a constructor?
    What is the definition of a higher-order function?
    Can you give an example for destructuring an object or an array?
    ES6 Template Literals offer a lot of flexibility in generating strings, can you give an example?
    Can you give an example of a curry function and why this syntax offers an advantage?
    What are the benefits of using spread syntax and how is it different from rest syntax?
    How can you share code between files?
    Why you might want to create static class members?
