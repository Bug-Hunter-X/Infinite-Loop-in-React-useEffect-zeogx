# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: creating an infinite loop by incorrectly using the dependency array.

## The Bug

The `bug.js` file contains a component that attempts to increment a state variable within the `useEffect` hook without specifying any dependencies. This leads to an infinite loop because every state update triggers a re-render, which in turn triggers the `useEffect` hook again.

## The Solution

The `bugSolution.js` file demonstrates how to fix the issue. By adding an empty dependency array `[]`, we ensure the `useEffect` hook only runs once after the initial render.