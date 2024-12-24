# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript closure issue that often arises when using `setTimeout` within a loop. The problem stems from how closures capture variables from their surrounding scope.

## Bug Description
The `bug.js` file contains a function that uses `setTimeout` to log values from a loop. Due to the way closures work in JavaScript, all the `setTimeout` callbacks will log the final value of `i` (which is 10) instead of the expected sequence of 0 to 9.

## Solution
The `bugSolution.js` file demonstrates a solution using an immediately invoked function expression (IIFE) to create a new scope for each iteration, ensuring that the correct value of `i` is captured for each callback.

## How to run
1. Clone this repository.
2. Open `bug.js` and `bugSolution.js` in a JavaScript environment (browser console, Node.js, etc.).
3. Run the functions and observe the output.  `bug.js` will show the unexpected behavior, while `bugSolution.js` will show the corrected output.