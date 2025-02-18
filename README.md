# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications involving the `useEffect` hook: an infinite loop caused by missing dependencies.

## The Bug

The `bug.js` file contains a React component that increments a counter.  The `useEffect` hook logs a message to the console after every render.  However, because `count` is not included in the `useEffect` dependency array, the effect runs after every render, triggering a new re-render and creating an infinite loop. 

## The Solution

The `bugSolution.js` file shows the corrected code.  By adding `count` to the dependency array, the effect now only runs when the `count` value changes, resolving the infinite loop.

## How to reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Open your browser to `http://localhost:3000` and observe the behavior. 
6. Compare the output and performance between bug.js and bugSolution.js.