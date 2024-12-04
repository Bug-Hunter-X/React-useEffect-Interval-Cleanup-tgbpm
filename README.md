# React useEffect setInterval Memory Leak
This repository demonstrates a common error in React applications involving the use of `setInterval` within the `useEffect` hook, which leads to a memory leak if not properly handled.

## Bug Description
The `MyComponent` component uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts, resulting in a memory leak.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console. You'll see the counter incrementing, but the interval will continue running even after the component is unmounted, causing a memory leak.

## Solution
The `bugSolution.js` file provides a corrected version of the component, which includes a cleanup function to clear the interval using `clearInterval` when the component unmounts.