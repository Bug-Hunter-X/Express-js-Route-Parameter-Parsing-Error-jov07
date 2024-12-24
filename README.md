## Express.js Route Parameter Parsing Error
This repository demonstrates a common error in Express.js route parameter handling and its solution. The bug occurs when a route parameter is expected to be a number but receives a non-numeric value.  The provided code lacks error handling for this scenario. The solution adds comprehensive error handling to gracefully manage non-numeric parameters.

**Bug:** The original code attempts to parse a user ID from the route parameters without checking if the parameter is a valid number. If a non-numeric ID is provided, the `parseInt` function returns `NaN`, leading to an unsuccessful search and potentially causing a server error or unexpected behavior.

**Solution:** The improved code handles this scenario gracefully by first checking if the `userId` is a valid number using `isNaN`. If not, it returns an appropriate HTTP error response indicating the invalid parameter. This prevents crashes and improves the overall robustness of the application.
