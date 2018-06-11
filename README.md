# Eloquent Javascript

Notes on Eloquent Javascript 3rd Edition [book link](http://eloquentjavascript.net/)

## Table of Contents

<!-- TOC -->

- [Eloquent Javascript](#eloquent-javascript)
  - [Table of Contents](#table-of-contents)
  - [Progress](#progress)
  - [Introduction](#introduction)
  - [Chapter 01: Values, Types, and Operators](#chapter-01-values-types-and-operators)
    - [Type: Numbers](#type-numbers)
    - [Type: Strings](#type-strings)
    - [Operators: Unary, Binary, and Ternary](#operators-unary-binary-and-ternary)
    - [Type: Boolean](#type-boolean)
    - [Comparison Operators: Always Return a Boolean](#comparison-operators-always-return-a-boolean)
    - [Logical Operators](#logical-operators)
    - [Type: Empty Values](#type-empty-values)
    - [Type Coercion](#type-coercion)
  - [Chapter 02: Program Structure](#chapter-02-program-structure)
    - [Expressions and Statements](#expressions-and-statements)
    - [Bindings `===` Variables: `const, let, var`](#bindings--variables-const-let-var)
    - [Type: Functions](#type-functions)
    - [Control Flow: Conditional Execution](#control-flow-conditional-execution)
  - [Exercises: Chapter 02](#exercises-chapter-02)
    - [Looping a Triangle](#looping-a-triangle)
    - [FizzBuzz](#fizzbuzz)
    - [Chessboard](#chessboard)
  - [Chapter 03: Functions](#chapter-03-functions)
    - [Type: Function](#type-function)
    - [Bindings and Scope](#bindings-and-scope)
    - [Three-Approaches to Define a Function](#three-approaches-to-define-a-function)
    - [Function Arguments](#function-arguments)
    - [Closure](#closure)
    - [Recursion](#recursion)
    - [Two-Types of Functions](#two-types-of-functions)
  - [Exercises: Chapter03](#exercises-chapter03)
    - [Minimum](#minimum)
    - [Recursion Exercise](#recursion-exercise)
    - [Bean Counting](#bean-counting)
  - [Chapter 04: Data Structures: Objects and Arrays](#chapter-04-data-structures-objects-and-arrays)
    - [Properties](#properties)
    - [Methods](#methods)
    - [Exercises: Chapter 04](#exercises-chapter-04)
      - [The Sum of a Range](#the-sum-of-a-range)
      - [Reversing an Array](#reversing-an-array)
      - [A List](#a-list)
      - [Deep Comparison](#deep-comparison)

<!-- /TOC -->

## Progress

- [X] ~~*Introduction*~~ [2018-05-21]
- [X] ~~*Chapter 01: Values, Types, and Operators*~~ [2018-05-22]
- [X] ~~*Chapter 02: Program Structure*~~ [2018-05-23]
- [X] ~~*Chapter 03: Functions*~~ [2018-05-25]
- [X] ~~*Chapter 04: Data Structures: Objects and Arrays*~~ [2018-06-09]
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

## Introduction

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

## Chapter 01: Values, Types, and Operators

### Type: Numbers

- JavaScript uses 64-bits to store numbers
- `13` or `9.81` or `2.998e8`
- Operators: `*`, `/`, `+`, `-`, `%` (modulo/remainder)
- Special Numbers:  `Infinity`, `-Infinity`, `NaN`

### Type: Strings

- Strings are wrapped by single quotes, double quotes, or backticks
- `\` servers as an escape character when used inside a string
- `\n` new line character, `\t` tab character
- JavaScript uses 16-bits to represent string characters
- `+` concatenate operator when used on strings
- Strings that use backticks are called _template literals_
  - `${}` javascript lives inside curly brackets

### Operators: Unary, Binary, and Ternary

- Binary Operators: `* / + - % > < >= <= === == != !==`
- Unary Operators: `typeof`, returns a string value
- Ternary Operators: `boolean ? do if true : do if false`

### Type: Boolean

- `true` or `false`

### Comparison Operators: Always Return a Boolean

- `>, >=, <, <=, ==, ===, !=, !==`, comparison operators always return a boolean
- _Note:_ Uppercase characters < lowercase characters (e.g. `'Z' < 'a' = true`)
- There is only one value in JavaScript that is not equal to itself, and that is `NaN`
  - `NaN == NaN` returns `false`

### Logical Operators

- JavaScript supports three logical operators: _and, or, and not_
- `&&` the logical _and_ operator returns `true` if both sides evaluate to `true`
- `||` the logical _or_ operator return `true` if either side evaluates to true
- `!` the logical _not_ operator returns the flips the value given to it `!true` produes `false`
- `? :` the _conditional_ operator is the only ternary operator in JavaScript. It works like a fancy `if else`

### Type: Empty Values

- `null` purposeful absence of value
- `undefined` program generated absence of value (indicative of a bug)

### Type Coercion

- _When code misbehaves, look for unintended Type Coercion_
- `null == undefined` => `true`
- `null == 0` => `false`
- The above is useful when testing if a variable has an assigned value
- `variable || default` can be used to return a `default` value if `variable` evaluates to `falsy`
- Logical operators are evaluated left to right, and will short-circuit when logical to do so.

## Chapter 02: Program Structure

### Expressions and Statements

- An `expression` is a fragment of code that produces a value
- A program is a list of `statements`

### Bindings `===` Variables: `const, let, var`

- Bindings/Variables are used to remember values
- To declare a binding/variable, you must use a binding _keyword_: `const`, `let`, or `var`
- `const` stands for _constant_. A `const` binding are block-scope and can't be reassigned a value. Const bindings point to a constant value once declared.
- `let` bindings are block-scope and can be reassigned  values after being declared
- `var` binding are function-scope and can be reassigned values after being declared

### Type: Functions

- Executing a function is called _invoking, calling or applying_ the function
- _Arguments_ are values passed into a function and wrapped in `( )`
- When a function produces a value, it is said to _return_ a value.

### Control Flow: Conditional Execution

- `if` `else if` `else`
- `while`
- `do while` similar to `while` but will execute at least once
- `for` loops `for (initialize, exit condition check, stepping)`
- `break` will exit out of conditional loops
- `continue` jumps to next iteration of the loop
- `count++` returns `count` then _increments_ `count`
- `++count` _increments_ `count` then returns `count`
- `count--` and `--count` works similar but _decrements_ `count`
- `switch` `case` `default`

```javascript
switch (condition) {
  case check1:
  something
  break
  case check2:
  dosomethingelse
  break
  default:
  dothisbydefault
  break
}
```

## Exercises: Chapter 02

- Solutions found at [Eloquent JavaScript Solutions](https://eloquentjavascript.net/code#2)

### Looping a Triangle

```javascript
let output = ''
for (let i = 0; i < 7; i++) {
  console.log(output += '#')
}
```

### FizzBuzz

```javascript
// Solution 1
for (let i = 1; i <= 100; i++) {
  if (i % 3 === 0 && i % 5 === 0) {
    console.log('FizzBuzz')
  } else if (i % 3 === 0) {
    console.log('Fizz')
  } else if (i % 5 === 0) {
    console.log('Buzz')
  } else {
    console.log(i)
  }
}
```

```javascript
// Solution 2
for (let i = 1; i <= 100; i++) {
  let word = ''
  if (i % 3 === 0) word += 'Fizz'
  if (i % 5 === 0) word += 'Buzz'
  console.log( word || i)
}
```

### Chessboard

```javascript
let size = 8
let board = ''
for (let i = 0; i < size; i++) {
  for (let j = 0; j < size; j++) {
    if ((i + j) % 2 === 0) {
      board += ' '
    } else {
      board += '#'
    }
  }
  board += '\n'
}
```

## Chapter 03: Functions

### Type: Function

>"People think that computer science is the art of geniuses but the actual reality is the opposite, just many people doing things that build on each other, like a wall of mini stones." - Donald Knuth

- Functions are declared with the _function_ keyword
- Functions consist of a set of _parameters_ and a _body_
- The function _body_ contains the statements that are executed when the function is called.

### Bindings and Scope

- _scope_ refers to where bindings are accessible in a program
- _global_ bindings are accessible in the entire program. These are variables defined outside of any function or block.
- _local_ bindings are accessible only within the function or block where they are declared
- `let` and `const` are block-scoped
- `var` is function-scoped

### Three-Approaches to Define a Function

```javascript
// FUNCTION DECLARATION
// function hoisted to top
square(5) // returns 25
function square(5) {
  return x * x
}
square(5) // returns 25
```

```javascript
// FUNCTION STATEMENT
// function not hoisted to top
square(5) // square is not defined
const square = function (x) {
  return x * x
}
square(5) // returns 25
```

```javascript
// FAT-ARROW FUNCTION STATEMENT
// function not hoisted to top
square1(5) // square1 is not defined
square2(5) // square2 is not defined
const square1 = x => x * x

const square2 = (x) => {
  return x * x
}
square1(5) // returns 25
square2(5) // returns 25
```

### Function Arguments

- Use `=` after a function argument to assign a default value

```javascript
function power(base, exponent = 2) {
  return Math.pow(base, exponent)
}
```

### Closure

- The ability to reference a specific instance of a a local binding in an enclosing scope is called _closure_
- A function that references bindings from local scopes around it is called _a closure_
- _closure_ is the ability of a function to remember/reference a binding that was declared outside its local scope.

### Recursion

- _Recursion_ is when a function calls itself, until it doesn't.

### Two-Types of Functions

- Return value functions - pure functions are a subset
- Side-Effect functions

## Exercises: Chapter03

### Minimum

```javascript
function min (x, y) {
  return (x <=  y) ? x : y
}
```

### Recursion Exercise

```javascript
function isEven (n) {
  if (n < 0) return n = -n
  if (n === 0) return true
  if (n === 1) return false
  return isEven(n - 2)
}
```

```javascript
// with helper function
function isEvenHelper(n) {
  if (n === 0) return true
  if (n === 1) return false
  return isEvenHelper(n - 2)
}

function isEven(n) {
  if (n < 0) return n = -n
  return isEvenHelper(n)
}
```

### Bean Counting

```javascript
function countBs (str) {
  let count = 0
  for (let i = 0; i < str.length; i++) {
    if (str[i] === 'B') count++
  }
  return count
}
```

```javascript
function countChar (str, char) {
  let count = 0
  for (let i = 0; i < str.length; i++) {
    if (str[i] === char) count++
  }
  return count
}
```

## Chapter 04: Data Structures: Objects and Arrays

### Properties

- _Properties_ on objects can be accessed via two methods:
  - _dot-notation_: `array.length`
  - _bracket-notation_: `array['length']`
- _Bracket-notation_: Evaluates argument inside brackets before fetching property value

### Methods

- _Methods_ are functions inside objects
- `delete obj.property` removes `property` from `obj`
- `'str' in object`: _in_ binary operator returns boolean
- `Object.keys(obj)`: returns string array of keys
- `array.indexOf(value)`: finds the array index of `value` or return `-1` if not found
- `.slice(start,end)`: returns a slice of an array; `start` index is inclusive; `end` index is exclusive
- `array1.concat(array2)`: joins two arrays
- `Object.assign(targetObject,{Object Literal})`: adds properties to targetObject

```javascript
function removeIndex(array, index) {
  array.slice(0,index).concat(array.slice(index+1))
}
```

- String methods: `.trim()` `.padStart(length,char)` `.join('')` `.split('')`
- Rest parameter: `function (...lastParameter)`
- _Spread operator_: `function(...[array])`
- `JSON.stringify(object)` and `JSON.parse(payload)`
- `for (let element of array)`: fancy array `for` loop

### Exercises: Chapter 04

#### The Sum of a Range

```javascript
function range (start, end, step = start < end ? 1 : -1) {
  let array = []
  if (start <= end) {
    for (let i = start; i <= end; i =+ step) array.push(i)
  } else {
    for (let i = start; i >= end; i =+ step) array.push(i)
  }
  return array
}

function sum(array) {
  total = 0
  for (let ele of array) {
    total += ele
  }
  return total
}

console.log(sum(range(9, 2, -3))) // 18
```

#### Reversing an Array

```javascript
function reverseArray (array) {
  let revArray = []
  for (let item of array) revArray.unshift(item)
  return revArray
}

function reverseArrayInPlace (array) {
  const size = array.length
  for (let i = 0; i < Math.floor(size / 2); i++) {
    let temp = array[i]
    array[i] = array[size - 1 - i]
    array[size - 1 - i] = temp
  }
  return array
}

console.log(reverseArray([ 1, 2, 3 ])) // [3, 2, 1]

let testArray = [1, 2, 3]
console.log(reverseArrayInPlace(testArray)) // [3, 2, 1]
console.log(testArray) // [3, 2, 1]
```

#### A List

```javascript
let array = [1, 2]
function arrayToList (array) {
  const list = {}
  let node = {}
  while (array.length) {
    const curValue = array.pop()
    list.value = curValue

    if (list.rest === undefined) {
      list.rest = null
    } else {
      list.rest = node
    }

    node = {
      value: list.value,
      rest: list.rest
    }
  }
  return list
}

const list = arrayToList(array)
console.log(list) // list = {value: 1, rest: {value: 2, rest: null}}

function listToArray (list) {
  const array = []
  if (list.value) {
    array.push(list.value)
  } else {
    return array
  }

  while (list.rest) {
    list = list.rest
    array.push(list.value)
  }
  return array
}

console.log(listToArray(list)) // array = [1, 2]

function prepend (newValue, list) {
  const node = { value: list.value, rest: list.rest }
  if (list.value) {
    list.value = newValue
    list.rest = node
  } else {
    list.value = newValue
    list.rest = null
  }
  return list
}

console.log(prepend(0, list)) // list = {value: 0, rest: {value: 1, rest: {value: 2, rest: null}}}

function nth (list, index) {
  let nthValue = list.value
  if (list.value === undefined || list.value === null) return undefined
  while (index) {
    index--
    list = list.rest
    if (!list.rest) {
      return undefined
    } else {
      nthValue = list.value
    }
  }
  return nthValue
}

function recursiveNth (list, index) {
  let nthValue = list.value
  if (list.value === undefined || list.value === null) return undefined
  while (index) {
    index--
    if (!list.rest) return undefined
    return recursiveNth(list.rest, index)
  }
  return nthValue
}

console.log(nth(0, list)) // 0
console.log(nth(1, list)) // 1
console.log(nth(2, list)) // 2
console.log(nth(3, list)) // undefined

// same for recursiveNth

```

#### Deep Comparison

```javascript

```