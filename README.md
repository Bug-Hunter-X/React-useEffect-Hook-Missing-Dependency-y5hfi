# React useEffect Hook Missing Dependency

This repository demonstrates a common error in React's `useEffect` hook: omitting dependencies in the dependency array.  This can lead to unexpected behavior, such as infinite loops or stale closures.

The `bug.js` file contains the erroneous code.  The `bugSolution.js` file provides the corrected implementation.

## Bug
The original code omits the `count` variable from the dependency array in `useEffect`. This means the effect runs only once after the initial render. Even if the component unmounts, the interval continues to update the count. 

## Solution
The corrected code includes `count` in the dependency array. This ensures the effect only runs when the value of `count` changes, and the interval is correctly cleared when the component unmounts. 