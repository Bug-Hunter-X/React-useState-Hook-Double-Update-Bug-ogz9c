# React useState Hook Double Update Bug

This repository demonstrates a common but subtle bug in React applications involving the `useState` hook and multiple state updates within a single render cycle.  The bug arises because React batches state updates for performance optimization.  When you update state multiple times rapidly, React might not use the most up-to-date value in subsequent updates, resulting in unexpected behavior.

## Bug Description:

The `bug.js` file contains a simple counter component that increments the count when a button is clicked. However, due to a double `setCount` call within the `handleClick` function, the count doesn't increment correctly. The second update uses a stale value of `count`.

## Solution:

The `bugSolution.js` file demonstrates a solution to this bug using the functional update form of `setCount`, ensuring that the update always uses the latest state value.  This approach ensures the counter increments properly.

## How to Run:

1. Clone this repository.
2. Navigate to the directory in your terminal.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.