# MongoDB $inc Operator Error

This repository contains a simple example of an error that can occur when using the `$inc` operator in MongoDB.

The `$inc` operator is used to increment a numeric field by a specified value.  However, if you provide a string value to the `$inc` operator, MongoDB will throw an error.

## Bug

The `bug.js` file contains the following code:

```javascript
// Incorrect use of $inc operator
db.collection.updateOne({ _id: 1 }, { $inc: { field: '1' } });
```

This code attempts to increment the `field` field by the string value `'1'`. This will result in an error.

## Solution

The `bugSolution.js` file contains the corrected code:

```javascript
// Correct use of $inc operator
db.collection.updateOne({ _id: 1 }, { $inc: { field: 1 } });
```

This code correctly increments the `field` field by the numeric value `1`.
