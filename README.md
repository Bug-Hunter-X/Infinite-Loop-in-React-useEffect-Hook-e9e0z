# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook.  The component experiences an infinite loop because the effect function lacks a dependency array, causing it to run on every render, leading to a constant state update and re-render cycle.

## Bug Description
The `useEffect` hook in the provided `MyComponent` continuously updates the state (`count`), triggering infinite re-renders. This can lead to browser crashes or significant performance issues.

## Solution
The solution involves adding a dependency array to the `useEffect` hook, ensuring it only runs when specified dependencies change. In this case, the `count` state is the only dependency.