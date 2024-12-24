# React SetInterval Memory Leak
This repository demonstrates a common error in React components that use `setInterval` within the `useEffect` hook without proper cleanup. This can lead to memory leaks.

## Bug Description:
The `MyComponent` uses `setInterval` to update the count every second. However, it does not include a cleanup function to clear the interval when the component unmounts. This causes the interval to continue running even after the component is no longer rendered, leading to a memory leak.

## Bug Solution:
The solution involves adding a return function inside the `useEffect` hook to clear the interval when the component unmounts.  This ensures that the interval is properly cleaned up, preventing memory leaks.