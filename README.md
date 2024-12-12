# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling when dealing with user input.  Specifically, the provided code attempts to access a user based on an ID parameter, but fails to handle cases where the ID is invalid (e.g., not a number, out of range).  This can lead to unexpected behavior or application crashes.

## Bug
The `bug.js` file contains the erroneous code.  It attempts to parse the user ID as an integer and directly uses it to find a user in a (simulated) `users` array.  No error handling is implemented for cases where `parseInt(userId)` fails or the user is not found.

## Solution
The `bugSolution.js` file provides a corrected version. It includes comprehensive error handling to validate the user ID and gracefully handle cases where the user is not found, returning appropriate HTTP status codes.