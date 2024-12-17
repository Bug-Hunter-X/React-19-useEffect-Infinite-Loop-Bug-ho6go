# React 19 useEffect Infinite Loop Bug

This repository demonstrates a common but subtle bug in React 19's `useEffect` hook that can lead to an infinite loop.  The bug arises from incorrect state update logic within the `useEffect` dependency array.  The solution shows how to fix this by properly managing state updates and avoiding unintended infinite loops.

## Bug Description
The bug occurs when using `useEffect` with a state variable in the dependency array. If the update logic within `useEffect` causes the state to change in a way that triggers the effect again infinitely, you have an infinite loop.  This example demonstrates how an infinite loop can be created by resetting state based on the current value of state.