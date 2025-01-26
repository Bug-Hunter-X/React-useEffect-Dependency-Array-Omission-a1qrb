# React useEffect Dependency Array Omission

This repository demonstrates a common error in React's `useEffect` hook: omitting necessary variables from the dependency array.  This can lead to unexpected behavior, such as infinite loops or incorrect updates.

## The Bug

The `bug.js` file contains a `MyComponent` that uses `useEffect` to log the current count. However, the `count` variable is missing from the dependency array.  This causes the effect to re-run on every render, regardless of whether `count` has actually changed. 

## The Solution

The `bugSolution.js` file corrects this issue by including `count` in the dependency array.  Now, the effect only runs when `count` changes.