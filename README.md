# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React's `useEffect` hook where an infinite loop occurs due to a missing dependency in the dependency array.

## Bug Description
The `useEffect` hook is used to perform side effects after a component renders.  If the dependency array is missing a value that changes on each render, the effect will run repeatedly, leading to an infinite loop and performance issues.  This example shows a `count` variable that is updated by a button; however, the `useEffect` hook doesn't include the `count` variable in its dependency array, which leads to the infinite loop.

## Solution
The solution is to include the `count` variable in the dependency array. This ensures the effect only runs when the `count` variable changes.