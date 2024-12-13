# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  lack of error handling for invalid input parameters. The example shows a route that fetches a user by ID.  If the ID is not a valid integer, the code throws an error. 

The `bug.js` file contains the erroneous code, and `bugSolution.js` provides the corrected version with appropriate error handling.

## Bug

The `bug.js` file attempts to parse the user ID from the request parameters as an integer but lacks proper error handling. If the ID is not a number, the `parseInt()` function will return `NaN`, which can cause unexpected behavior or application crashes.

## Solution

The `bugSolution.js` file addresses the bug by adding error handling. It checks if the parsed ID is actually a number before proceeding.  If the ID is invalid or the user is not found, it sends an appropriate HTTP response (400 Bad Request or 404 Not Found).