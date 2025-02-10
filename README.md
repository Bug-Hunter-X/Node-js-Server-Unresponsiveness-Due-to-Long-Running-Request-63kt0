# Node.js Server Unresponsiveness
This repository demonstrates a common issue in Node.js servers: unresponsiveness due to long-running requests.  A simple HTTP server is created that simulates a long-running task blocking the event loop.

## Problem
The provided `server.js` code creates an HTTP server that processes requests. A long-running task (simulated by a `while` loop) is executed during request processing, blocking the event loop. This prevents the server from responding to other requests, leading to unresponsiveness and potential crashes.

## Solution
The solution in `serverSolution.js` addresses this by using asynchronous operations and non-blocking I/O, preventing the server from hanging. This ensures that the event loop continues processing other tasks while the long-running operation runs concurrently.