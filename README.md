# Unusually Slow Response Time in Node.js Express Server

This repository demonstrates a common issue in Node.js Express servers where response times are unexpectedly slow due to an unintentional delay in the response handling.  The original `server.js` shows a simple Express server that introduces a 5-second delay before sending a response.  The solution in `serverSolution.js` demonstrates the correct way to avoid such delays.

## How to reproduce:

1. Clone the repository.
2. Run `node server.js`.
3. Make a request to `http://localhost:3000`. Observe the significant delay. 
4. Run `node serverSolution.js` and repeat step 3 to see immediate response.

## Solution:
The solution involves removing the `setTimeout` function. This is a simplified example to demonstrate this specific kind of problem.  In real world scenarios, such unexpected delays can be caused by slow database queries, network I/O, or other blocking operations.