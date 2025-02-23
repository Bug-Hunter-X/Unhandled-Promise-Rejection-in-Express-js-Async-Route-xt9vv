# Unhandled Promise Rejection in Express.js Async Route

This repository demonstrates a common error in Express.js applications: unhandled promise rejections in asynchronous routes.  The `bug.js` file showcases the issue, while `bugSolution.js` provides a corrected version with proper error handling.

## Bug Description

The `bug.js` file defines a simple Express.js route that performs an asynchronous operation using `Promise`.  However, it lacks a `.catch` block to handle potential errors during this operation.  If the asynchronous operation fails, the application will silently fail without any indication, making it harder to debug.

## Solution

The `bugSolution.js` file addresses this by adding a `.catch` block to the asynchronous route. This block logs the error to the console and sends an appropriate error response to the client, ensuring that the application doesn't crash and provides informative feedback to the user.