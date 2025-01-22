# Inefficient useEffect in React Component

This repository demonstrates a common mistake in React's `useEffect` hook: adding no dependency array causing the effect to run on every render. This leads to unnecessary re-renders and performance problems.  The solution shows how to correctly use the dependency array to improve efficiency.

## Bug
The `useEffect` hook in `bug.js` is missing a dependency array. This means that it will run after every render, not just when the `count` variable changes. This will lead to unnecessary logging and can significantly impact performance in more complex components.

## Solution
The `bugSolution.js` demonstrates the correct way to use `useEffect` with a dependency array `[count]`. Now, the effect will only run when `count` changes, improving performance.