# React useEffect setInterval Memory Leak

This repository demonstrates a common React bug involving memory leaks when using `setInterval` within the `useEffect` hook without proper cleanup.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides a corrected version.

## Problem

The original code fails to clear the interval using `clearInterval` when the component unmounts. This results in the interval continuing to run indefinitely, causing a memory leak and potentially affecting performance.

## Solution

The solution involves adding a cleanup function to the `useEffect` hook's return value. This function calls `clearInterval` to stop the interval when the component is unmounted or when the dependencies change.
