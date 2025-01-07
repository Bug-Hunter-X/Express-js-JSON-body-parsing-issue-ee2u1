# Express.js JSON Body Parsing Issue

This repository demonstrates a common issue when working with JSON request bodies in Express.js applications: failure to parse the JSON body if the `Content-Type` header is missing or incorrect. 

The `bug.js` file showcases the problematic code, while `bugSolution.js` provides the solution. 

## Bug
The bug lies in the fact that if a client sends a POST request to `/data` without setting the `Content-Type` header to `application/json`, Express.js's `express.json()` middleware will not parse the request body, resulting in `req.body` being empty.  This can lead to unexpected behavior and errors in your application.

## Solution
The solution involves ensuring that the client sends the correct `Content-Type` header, or alternatively, handling cases where the header is missing or incorrect in the server-side code. The solution also shows how to handle errors appropriately when parsing the request body.