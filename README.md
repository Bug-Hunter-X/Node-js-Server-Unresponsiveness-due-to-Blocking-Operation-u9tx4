# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js where a long-running synchronous operation blocks the event loop, causing the server to become unresponsive.  The `server.js` file contains the buggy code, and `serverSolution.js` provides a solution using asynchronous operations.

## Bug Description

The server performs a 5-second synchronous loop, which blocks the event loop.  During this time, the server is unable to process other requests and effectively becomes unresponsive.  This is a classic example of a performance bottleneck caused by blocking I/O.

## Solution

The solution involves refactoring the code to use asynchronous operations (e.g., using `setTimeout`, promises, or async/await) to avoid blocking the event loop. The `serverSolution.js` file demonstrates this.