# Javascript Intro

[Javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) is the language of the web. While tasks like page structure and
styling are handled by HTML & CSS, page interactivity falls within the domain
of Javascript.
The [MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web) are a phenomenal resource for getting started!

## 1. [Language Basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics#language_basics_crash_course)

- Expressions/statements `console.log('this line is a statement');`
- [Variable assignent](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics#variables) `var x = 4`
- [Data types](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types) `number`, `string`, `array`, ...
- [Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)
- [Conditional statements](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/conditionals#if...else_statements) `if (...) {}`
- Logical operators `&&`, `||`, `==`, ...
- [Loops](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration) `while (...)`, `for (...)`
- [Comments](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics#comments) `functionCall() //descriptive comment, which is not executed`
- [String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#description) properties & methods `.length`, `.split(",")`, ...
- [String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#description) manipulation, concatenation `"hello" + " " + "world"`
- [Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)
- [Array instantiation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#constructor) `Array.of(...)`, `Array(...)`, `Array.from(...)`, ...
- Array [properties](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#instance_properties) & [methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#instance_methods) `.length`, `.includes()`, ...

```javascript
function askNicely(name) {
  console.log("Hi, " + name + ". Could you please get me a coffee?");
}

var interns = ["Nadia", "Jared", "Pohla"];

for (var index = 0; index < interns.length; index++) {
  var name = interns[index];
  askNicely(name);
  if (name == "Jared") {
    console.log("Oh, and could you leave room for cream, please?");
  }
}
```

## 2. More advanced concepts

- [Falsy values](https://developer.mozilla.org/en-US/docs/Glossary/Falsy) `false`, `0`, `""`, ...
- [Truthy values](https://developer.mozilla.org/en-US/docs/Glossary/Truthy) `true`, `{}`, `1`, ...
- [Global vs. Block-scoping](https://developer.mozilla.org/en-US/docs/Glossary/Scope)
- [Ternary operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator) `some_value ? console.log('true') : console.log('false)`

## 3. Even _more_ advanced concepts

- [Iterators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_Generators#iterators)
- [Higher-order array functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#instance_methods) `[...].map()`, `[...].filter()`, `[...].reduce()`, ...
- [Callback functions](https://developer.mozilla.org/en-US/docs/Glossary/Callback_function)
- [`Math` object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math) & its methods
- [`Date` object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) & its methods
- [Strict vs. loose equality](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness) `===` vs. (`==`)

## 4. ES6-specific Language Additions

- [`let`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) & [`const`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const) vs. [`var`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var)
- [Template literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals) `` hello, `${"world"}`! ``
- [Arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)
- [Destructuring](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment) `const [one, two] = [1, 2]`
- [`...rest` parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters#description)
- [`for _ of _` loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...of)
- [Spread operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)

## 5. [Modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)

- [Exporting from modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules#exporting_module_features)
  - Named exports `export const arrFn = () => ...`
  - Default export `export default () => {...}`
- [Importing from modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules#importing_features_into_your_script) `import defaultImport, { namedImport } from "./otherModule.js"`
- [Renaming imports/exports](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules#renaming_imports_and_exports) `import { namedImport as whatever } from "..."`
- Modules vs. scripts

## 6. [Asynchronous JS](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous)

- "Event loop"
- "Blocking" and "Non-blocking"
- `setTimeout()`, `setInterval()`

- Synchronous vs. Asynchronous

```javascript
const greet = () => console.log("hello");
greet();
console.log("world");
```

Outputs:

```
hello
world
```

```javascript
...
setTimeout(greet, 1000)
console.log('world')
```

Outputs:

```
world
...
hello
```

- [Promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) `fnThatReturnsPromise().then(...).catch(...)`
- [Callback functions](https://developer.mozilla.org/en-US/docs/Glossary/Callback_function) `fnThatReturnsPromise(]).then(() => console.log('done'))`
- [`async`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function) / [`await`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/await) syntax

## 7. Data-fetching

- [AJAX (Asynchronous JS And XML)](https://developer.mozilla.org/en-US/docs/Web/Guide/AJAX)
- [HTTP (HyperText Transfer Protocol)](https://developer.mozilla.org/en-US/docs/Web/HTTP)
- [JSON (JavaScript Object Notation)](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/JSON)
- [Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch)
- [Axios](https://axios-http.com/docs/example)

## 8. JS & the DOM

- [What is the DOM?](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction#dom_and_javascript)
- [HTML basics](https://developer.mozilla.org/en-US/docs/Glossary/HTML#concept_and_syntax)
  - HTML structure
  - HTML tags
  - Classes
  - IDs
- [DOM nodes, elements](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction#fundamental_data_types)
- [Accessing DOM elements](https://developer.mozilla.org/en-US/docs/Web/API/Document_object_model/Locating_DOM_elements_using_selectors)
  - `document.getElementById('foo')`
  - `document.querySelector('#foo, #bar')`
  - `document.querySelectorAll('#foo')`
- Manipulating DOM elements
  - `element.innerHTML = 'hello, world`
  - `element.classList.add('active')`
  - `element.classList.toggle('inactive')`
- Traversing the DOM
  - `element.parentNode;`
  - `element.nextElementSibling;`
  - `element.firstChild;`
- Accepting user input via the [`<form>` element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form)
- [HTML events](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events)
  - [`Event` object](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events#event_objects)
  - Event types ('scroll', 'onclick', 'onload', 'onsubmit', ...)
  - [`element.addEventListener('...', handlerFn)`](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events#using_addeventlistener)
  - [Event 'bubbling'](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events#event_bubbling_and_capture), and [how to avoid it](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events#fixing_the_problem_with_stoppropagation)
- [Web Storage API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API)
  - [`window.localStorage` object](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage)
