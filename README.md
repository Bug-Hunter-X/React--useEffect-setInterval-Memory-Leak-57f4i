# React useEffect setInterval Memory Leak

This repository demonstrates a common error in React: using `setInterval` within a `useEffect` hook without proper cleanup. This can lead to memory leaks and unexpected behavior.

## Bug

The `bug.js` file contains a component that uses `setInterval` to increment a counter every second. However, it lacks a cleanup function to clear the interval when the component unmounts.  This results in the interval continuing to run even after the component is no longer rendered, leading to a memory leak and potential performance issues.

## Solution

The `bugSolution.js` file shows the corrected code. The cleanup function within the `useEffect` hook now uses `clearInterval` to stop the interval when the component is unmounted, preventing memory leaks.

## How to Run

1. Clone this repository.
2. Run `npm install`
3. Run `npm start`