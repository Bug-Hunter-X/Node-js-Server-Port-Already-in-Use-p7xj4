# Node.js Server Port Already in Use

This repository demonstrates a common error in Node.js: attempting to start a server on a port that's already in use.  The example shows a simple HTTP server and the error handling that should be used to prevent crashes and provide informative messages to users.

## Problem

The provided `bug.js` file contains a basic HTTP server. If you run this and the port 8080 is already in use (e.g., by another instance of the server or a different application), the server will crash without a very user-friendly message.

## Solution

`bugSolution.js` demonstrates how to gracefully handle this error.  It uses an `error` listener on the server to catch the `EADDRINUSE` error and provide a more informative message to the user.

## How to Run

1.  Clone this repository.
2.  Navigate to the repository's directory in your terminal.
3.  Run `node bug.js` (this should likely fail if port 8080 is in use).
4.  Run `node bugSolution.js` (this will handle the error gracefully).