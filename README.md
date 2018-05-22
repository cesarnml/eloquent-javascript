# Table of Contents

<!-- TOC -->

- [Table of Contents](#table-of-contents)
  - [eloquent-javascript](#eloquent-javascript)
    - [Progress](#progress)
    - [Introduction](#introduction)
    - [Chapter 01: Values, Types, and Operators](#chapter-01-values-types-and-operators)
    - [Chapter 02: Program Structure](#chapter-02-program-structure)

<!-- /TOC -->

## eloquent-javascript

Notes on Eloquent Javascript 3rd Edition [book link](http://eloquentjavascript.net/)

### Progress

- [X] *Introduction* [2018-05-21]
- [X] *Chapter 01: Values, Types, and Operators* [2018-05-22]
- [ ] Chapter 02: Program Structure
- [ ] Chapter 03: Functions
- [ ] Chapter 04: Data Structures: Objects and Arrays
- [ ] Chapter 05: Higher-order Functions
- [ ] Chapter 06: The Secret Life of Objects
- [ ] Chapter 07: Project: A Robot
- [ ] Chapter 08: Bugs and Errors
- [ ] Chapter 09: Regular Expressions
- [ ] Chapter 10: Modules
- [ ] Chapter 11: Asynchronous Programming
- [ ] Chapter 12: Project: A Programming Language
- [ ] Chapter 13: JavaScript and the Browser
- [ ] Chapter 14: The Document Object Model
- [ ] Chapter 15: Handling Events
- [ ] Chapter 16: Project: A Platform Game
- [ ] Chapter 17: Drawing on Canvas
- [ ] Chapter 18: HTTP and Forms
- [ ] Chapter 19: Project: A Pixel Art Editor
- [ ] Chapter 20: Node.js
- [ ] Chapter 21: Project: Skill-Sharing Website

### Introduction

- "Because computers are dumb, pedantic beasts, programming is fundamentally tedious and frustrating"
- "Programming, it turns out, is hard"
- "Learning is hard work, but everything you learn is yours, and will make subsequent learning easier"
> "When action grows unprofitable, gather information; when information grows unprofitable, sleep" - Ursula K. Le Guin, _The Left Hand of Darkness_
- "A program is a building of thought. It is costless to build, it is weightless, and it grows easily under our typing hands."
- "Keeping programs **under control** is the main problem of programming"
- "A sense of what a good program looks like is developed in practice, not learned from a list of rules."
- JavaScript was created in 1995 (Netscape Navigator) by Brendan Eich

```javascript
// Calculate nth Fibonacci Number - Recursion!

function factorial (n) {
  if (n === 0) {
    return 1
  } else {
    return factorial(n - 1) * n
  }
}
```

### Chapter 01: Values, Types, and Operators

- **Type: Numbers**
  - JavaScript uses 64-bits to store numbers
  - `13` or `9.81` or `2.998e8`
  - Operators: `*`, `/`, `+`, `-`, `%` (modulo/remainder)
  - Special Numbers:  `Infinity`, `-Infinity`, `NaN`
- **Type: Strings**
  - Strings are wrapped by single quotes, double quotes, or backticks
  - `\` servers as an escape character when used inside a string
  - `\n` new line character, `\t` tab character
  - JavaScript uses 16-bits to represent string characters
  - `+` concatenate operator when used on strings
  - Strings that use backticks are called _template literals_
    - `${}` javascript lives inside curly brackets
- **Operators**
  - Binary Operators: `* / + - % > < >= <= === == != !==`
  - Unary Operators: `typeof`, returns a string value
  - Ternary Operators: `boolean ? do if true : do if false`
- **Type: Boolean**
  - `true` or `false`
- **Comparison Operators**
  - `>, >=, <, <=, ==, ===, !=, !==`, comparison operators always return a boolean
  - _Note:_ Uppercase characters < lowercase characters (e.g. `'Z' < 'a' = true`)
  - There is only one value in JavaScript that is not equal to itself, and that is `NaN`
    - `NaN == NaN` returns `false`
- **Logical Operators**
  - JavaScript supports three logical operators: _and, or, and not_ 
  - `&&` the logical _and_ operator returns `true` if both sides evaluate to `true`
  - `||` the logical _or_ operator return `true` if either side evaluates to true
  - `!` the logical _not_ operator returns the flips the value given to it `!true` produes `false`
  - `? : ` the _conditional_ operator is the only ternary operator in JavaScript. It works like a fancy `if else`
- **Empty Value**
  - `null` purposeful absence of value
  - `undefined` program generated absence of value (indicative of a bug)
- **Type Coercion**
  - _Just be aware of it when code misbehaves_
  - `null == undefined` => `true`
  - `null == 0` => `false`
  - The above is useful when testing if a variable has a real value assigned.
  - `this || default` can be used to return default value if this evaluates to falsy
  - Logical operators are evaluated left to right, and will short-circuit when logical to do so.

### Chapter 02: Program Structure
