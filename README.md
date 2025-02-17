# JavaScript Loose Equality and Null Checks

This repository demonstrates a common error in JavaScript related to loose equality (`==`) and null checks.  The issue arises when using loose equality to compare values, particularly when dealing with `null`.  Loose equality can lead to unexpected type coercion, causing null checks to fail.

## Bug

The original code may attempt to check for null using loose equality:

```javascript
if (a == null) { ... }
```
This can be problematic because `0 == null` evaluates to `false`, `'' == null` evaluates to `false`, and `false == null` evaluates to `false`.  The intended check might not accurately detect `null`. 

## Solution

The correct solution is to use strict equality (`===`) for null checks:
```javascript
if (a === null) { ... }
```
Strict equality does not perform type coercion, leading to more predictable and reliable null checks.