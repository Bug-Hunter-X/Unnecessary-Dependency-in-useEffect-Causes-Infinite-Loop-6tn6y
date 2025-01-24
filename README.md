# Unnecessary Dependency in useEffect Causes Infinite Loop

This example demonstrates a common error in React's `useEffect` hook where an unnecessary dependency leads to an infinite loop.

The `useEffect` hook in the original code has an unnecessary dependency array.  It will cause an infinite loop because every time the component renders, `count` will change, triggering the useEffect again, hence the infinite loop and unnecessary log messages. 
The solution fixes this by removing the unnecessary dependency and only firing the effect if needed. 

## How to Reproduce

1.  Clone the repository.
2.  Run `npm install`.
3.  Run `npm start`.
4.  Observe the console logs and the infinite loop.

## Solution

The solution demonstrates the correct usage of the dependency array in `useEffect`.
