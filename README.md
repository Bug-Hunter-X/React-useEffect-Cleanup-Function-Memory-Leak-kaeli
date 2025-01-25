# React useEffect Cleanup Function Memory Leak

This repository demonstrates a common React bug involving a missing return statement in the cleanup function of a `useEffect` hook, leading to memory leaks.  The example shows an event listener that's not properly removed when the component unmounts, causing potential issues.

## Bug Description

The `useEffect` hook is used to add an event listener (`keydown`). However, the cleanup function (the function returned by `useEffect`) is missing. Without a cleanup function, the listener remains attached even after the component is unmounted, causing a memory leak and potential unexpected behavior. 

## Solution

The solution includes adding a return statement to the `useEffect` hook that removes the event listener using `removeEventListener`. This ensures that the listener is properly cleaned up when the component is unmounted, preventing memory leaks and improving application stability. 
