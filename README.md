# Unresponsive Node.js Server Due to Blocking Operation

This repository demonstrates a common issue in Node.js applications: an unresponsive server caused by a long-running synchronous operation that blocks the event loop. The `server.js` file contains the buggy code, while `serverSolution.js` provides a solution using asynchronous operations.

## Problem

The server in `server.js` simulates a long-running operation using a `while` loop. This blocks the event loop, preventing the server from responding to new requests or handling existing ones efficiently.  This results in an unresponsive server.

## Solution

The solution in `serverSolution.js` demonstrates how to fix this issue using asynchronous techniques. Instead of a blocking `while` loop, asynchronous operations allow the event loop to continue processing other requests and events while the long-running task executes in the background.