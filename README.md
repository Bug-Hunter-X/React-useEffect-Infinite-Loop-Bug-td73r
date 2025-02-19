# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving an infinite loop within the `useEffect` hook. The bug arises from an incorrect condition within the `useEffect`'s dependency array, leading to continuous state updates and infinite rendering.

## Bug Description

The `MyComponent` functional component uses the `useState` hook to manage a `count` variable.  The `useEffect` hook is intended to reset the count to 0 if it exceeds 5. However, the implementation incorrectly causes an infinite loop because updating the count inside the `useEffect` triggers another render, which re-evaluates the condition and continues the cycle.

## Bug Solution

The solution modifies the `useEffect`'s logic to prevent the infinite loop. Instead of directly updating the `count` within the `useEffect` hook, the solution uses the previous state value and checks if it exceeded 5, preventing the infinite loop.
