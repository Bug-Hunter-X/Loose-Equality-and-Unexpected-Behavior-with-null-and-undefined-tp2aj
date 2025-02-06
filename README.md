# Loose Equality and Unexpected Behavior with null and undefined in JavaScript

This repository demonstrates a common JavaScript error related to loose equality (==) and the handling of null and undefined values.

## The Bug

The `foo` function attempts to handle `null` values, returning 0 in that case. However, it doesn't explicitly handle `undefined`.  When `undefined` is passed, the addition operation leads to `NaN` (Not a Number).

## The Solution

The solution uses strict equality (===) to explicitly check for null and undefined values, providing clear and expected results for all inputs.  This avoids the type coercion issues associated with loose equality.

## How to reproduce

1. Clone this repository.
2. Open `bug.js` to see the buggy implementation.
3. Run the code. You will see that calling the function with undefined produces NaN.
4. Open `bugSolution.js` to see the fixed implementation.
5. Run the corrected code to see that it handles null and undefined values as intended.