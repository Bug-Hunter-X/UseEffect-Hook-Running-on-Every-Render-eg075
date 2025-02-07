# React useEffect Hook Misuse

This repository demonstrates a common mistake in using the `useEffect` hook in React.  The provided `bug.js` file shows how omitting the dependency array causes the effect to run on every render, even if the state variable hasn't changed.  The `bugSolution.js` file shows the correct usage with the dependency array to fix this problem.

## Problem

The `useEffect` hook without a dependency array (or an empty array `[]`) runs after every render. This can lead to infinite loops, performance degradation, and unnecessary side effects. 

## Solution

The correct implementation should include a dependency array that specifies which variables to observe.  The effect will only run when one of the variables in this array changes.