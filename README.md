# Express.js JSON Body Parsing Bug

This repository demonstrates a common issue encountered when using Express.js to parse JSON request bodies: failure to handle empty or malformed JSON data.

## Bug Description
The provided Express.js server uses `express.json()` middleware to parse incoming JSON requests. However, it fails gracefully when the request body is empty or contains invalid JSON. Instead of returning an appropriate error response, it logs an empty object and proceeds as if the body was parsed successfully.

## Bug Reproduction
1. Clone this repository.
2. Run `npm install` to install the required dependencies.
3. Run `node bug.js` to start the server.
4. Send a POST request to `http://localhost:3000/data` with an empty body or an invalid JSON payload using tools like Postman or curl.
5. Observe that the server logs an empty object and sends a 'Data received' response, indicating it failed to handle the error correctly.

## Solution
The solution involves adding error handling to properly manage cases with empty or malformed JSON requests.  This is explained in detail in the solution file (bugSolution.js).
