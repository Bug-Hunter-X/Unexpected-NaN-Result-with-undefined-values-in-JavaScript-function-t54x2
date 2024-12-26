# Unexpected NaN Result with undefined values in JavaScript function

This repository demonstrates a common JavaScript error related to the handling of undefined values in functions designed to handle null values. The function `foo` aims to gracefully handle null inputs by returning 0. However, it unexpectedly returns `NaN` when encountering `undefined` arguments.

The `bug.js` file contains the erroneous code, while `bugSolution.js` provides a corrected version that addresses the issue.

## Bug Description
The function `foo` correctly returns 0 when either or both `a` and `b` are `null`. However, if either `a` or `b` is `undefined`, instead of returning a value like 0, it returns `NaN` which can lead to unexpected outcomes in applications.

## Solution
The bug is solved by explicitly checking for both `null` and `undefined` using the loose equality operator (==). This ensures the function handles both cases gracefully, returning a default value when undefined is encountered.