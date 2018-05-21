# Table of Contents

<!-- TOC -->

- [Table of Contents](#table-of-contents)
  - [eloquent-javascript](#eloquent-javascript)
    - [Progress](#progress)
    - [Introduction](#introduction)

<!-- /TOC -->

## eloquent-javascript

Notes on Eloquent Javascript 3rd Edition [book link](http://eloquentjavascript.net/)

### Progress

- [X] *Introduction* [2018-05-21]
- [ ] Chapter 01: Values, Types, and Operators
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

function factorial(n) {
  if (n === 0) {
    return 1
  } else {
    return factorial(n - 1) * n
  }
}
```