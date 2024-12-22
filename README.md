# React useEffect Hook Memory Leak

This example demonstrates a common mistake in React's `useEffect` hook that leads to memory leaks. The problem lies in the improper handling of the `setInterval` function, which is not correctly cleared when the component unmounts. This results in the interval continuing to run even after the component is removed from the DOM, leading to unnecessary resource consumption and potential performance issues.

The solution involves adding a cleanup function to the `useEffect` hook that clears the interval using `clearInterval` before the component is unmounted. This ensures that the interval is stopped, preventing the memory leak and improving the application's overall stability.