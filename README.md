# Unnecessary useEffect Dependency Warning in React 18+

This repository demonstrates a common error in React 18 and later related to the `useEffect` hook.  The example shows how including the state variable in the dependency array can lead to unnecessary re-renders and warnings.

## Problem

The `useEffect` hook is used to perform side effects after a component renders.  However, including state variables in the dependency array without a need can cause infinite loops or unnecessary re-renders.

## Solution

The solution involves removing the unnecessary state variables from the dependency array. If you need to run the side effect only after some other state or prop changes, add those other variables in the dependency array instead of the state variable that's triggering re-renders.