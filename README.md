# Unhandled Request in Express.js Route Handler

This repository demonstrates a common error in Express.js applications: forgetting to send a response in a route handler.

## Bug

The `bug.js` file contains an Express.js server with a route handler that logs a message to the console but doesn't send a response to the client. This results in the client receiving no response and potentially timing out.

## Solution

The `bugSolution.js` file demonstrates the corrected code.  The route handler now includes `res.send()` to send a response to the client.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `node bug.js`.
4. Make a request to `http://localhost:3000/` in your browser.  You'll observe that the server logs a message but the browser doesn't receive a response. 
5. Run `node bugSolution.js` and repeat the request. Now you should see a response in the browser. 