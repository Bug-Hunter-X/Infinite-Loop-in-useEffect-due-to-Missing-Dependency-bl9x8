# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The issue arises from omitting dependencies in the `useEffect` hook's second argument, leading to an infinite render loop.

## Bug Description
The `useEffect` hook in the provided `bug.js` file is intended to log the updated count to the console. However, because it lacks a dependency array, it runs after every render, causing the `setCount` function to update the state, trigger a re-render, and repeat the process indefinitely.

## Solution
The `bugSolution.js` file demonstrates the corrected code.  By including `[count]` as the dependency array, the `useEffect` hook only runs when the `count` state changes, resolving the infinite loop issue.

## How to reproduce
1. Clone the repository
2. Navigate to the project directory
3. Run `npm install` to install the necessary dependencies
4. Run `npm start` to start the development server.
5. Open your browser and observe the console output and the component behavior.