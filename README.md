# React 19 useEffect Infinite Loop Bug

This repository demonstrates a common bug in React 19 where an infinite loop occurs due to improper use of the `useEffect` hook.  The `useEffect` hook, when not used carefully, can lead to unexpected re-renders and crashes.

## Bug Description
The provided `MyComponent` uses `useEffect` without specifying dependencies. This causes the effect to run after every render, creating an infinite loop because the state update within the effect triggers another render.

## Solution
The solution involves correctly specifying the dependencies array in `useEffect`. By including `count` in the dependency array, the effect only runs when the `count` value changes.