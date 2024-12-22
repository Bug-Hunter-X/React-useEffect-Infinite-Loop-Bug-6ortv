# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook.  The bug is an infinite render loop caused by a missing dependency in the `useEffect` hook's dependency array.

## Bug Description
The `MyComponent` functional component uses `useState` to manage a count. The `useEffect` hook is intended to log the current count to the console after every render. However, because `count` is not listed in the dependency array, the effect runs after every render, causing a new state update and thus an infinite loop of re-renders.