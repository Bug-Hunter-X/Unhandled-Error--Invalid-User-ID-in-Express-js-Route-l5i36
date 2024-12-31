# Unhandled Error: Invalid User ID in Express.js Route

This repository demonstrates a common error in Express.js route handlers: insufficient error handling for invalid input parameters.  Specifically, the `/users/:id` route fails to gracefully handle cases where the `:id` parameter is not a valid integer.

## The Bug
The `bug.js` file contains an Express.js route handler that attempts to fetch a user by ID.  It uses `parseInt()` to convert the ID to an integer, but lacks error handling if the conversion fails.  This can result in unexpected errors or crashes.

## The Solution
The `bugSolution.js` file demonstrates a corrected version of the route handler.  It includes explicit error handling to check if `parseInt(userId)` is a valid integer and sends an appropriate error response if not.  This ensures the application handles invalid input gracefully and prevents unexpected errors.