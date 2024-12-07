# React UseEffect setInterval Memory Leak
This repository demonstrates a common mistake in React: using `setInterval` within a `useEffect` hook without proper cleanup.  This can lead to memory leaks and unexpected behavior in your application.

## The Problem
The `bug.js` file contains a component that uses `setInterval` to increment a counter every second. However, it lacks the necessary cleanup function to stop the interval when the component unmounts. This means the interval continues running even after the component is removed from the DOM, leading to a memory leak.

## The Solution
The `bugSolution.js` file demonstrates the corrected version.  It uses the return value of `useEffect` to provide a cleanup function that calls `clearInterval` to stop the interval when the component unmounts. This prevents the memory leak.

## How to run
1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.