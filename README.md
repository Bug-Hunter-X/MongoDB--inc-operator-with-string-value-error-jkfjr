# MongoDB $inc operator with string value error

This repository demonstrates a common error when using the `$inc` operator in MongoDB update operations. The `$inc` operator is used to increment a numerical value in a document. However, if a string value is provided, it may lead to unexpected behavior or silent failure. 

## Bug Description
The bug involves using a string value instead of a numeric value with the `$inc` operator in MongoDB.  This will either not update the field or it will silently fail to increment the value correctly.

## How to Reproduce
1.  Create a MongoDB collection named `myCollection` with a document that has a field named `count` with a numeric value.
2.  Run the provided Javascript code using a MongoDB driver. 
3.  Observe the outcome.

## Solution
Ensure that you provide a numeric value to the `$inc` operator. Do not use strings or other non-numeric values.  Convert any string values to numbers before using the operator.