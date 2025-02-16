# Ada Off-by-One Error Example
This example demonstrates a common off-by-one error in Ada when iterating over arrays.  Ada arrays are not zero-based; they start at their declared lower bound.  Incorrectly assuming a zero-based index can lead to runtime errors.

## The Bug
The `bug.ada` file contains code that attempts to iterate over an array using a loop that implicitly assumes a zero-based index. This leads to a `Constraint_Error` exception because the array index is out of bounds.

## The Solution
The `bugSolution.ada` file demonstrates the corrected code. It properly iterates over the array using the array's defined bounds.