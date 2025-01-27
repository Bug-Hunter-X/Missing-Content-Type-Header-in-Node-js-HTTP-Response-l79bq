# Missing Content-Type Header in Node.js HTTP Response

This repository demonstrates a common but easily overlooked error in Node.js HTTP servers: omitting the `Content-Type` header in the response.  This can cause unexpected behavior on the client-side, as the browser (or other client) may not correctly interpret the response body.

## Bug Description

The `bug.js` file shows an HTTP server that responds without specifying a `Content-Type` header.  This can result in the client receiving the response but not understanding how to handle it.  For example, a JSON response might be treated as plain text, leading to parsing errors.

## Solution

The `bugSolution.js` file demonstrates the correct way to handle this.  The `Content-Type` header is explicitly set to indicate the type of data being sent, enabling the client to process it correctly.

This simple fix prevents potential issues with client-side parsing and ensures a more robust and predictable HTTP server.