# Node.js Server Hanging on Long Requests

This repository demonstrates a common issue in Node.js servers: hanging on long-running requests.  The `server.js` file shows a server that blocks the event loop while processing a request. The `server-solution.js` provides a solution using async/await to prevent this blocking behavior. 

## Problem

Node.js is single-threaded.  A long-running operation in a request handler will block all other requests.  This results in an unresponsive server. 

## Solution

The solution is to use asynchronous operations using `async/await` or Promises. This allows the event loop to continue processing other requests while the long-running task executes in the background. 