# First Bad Version

## 1. Problem

There are some versions of a product. One version is bad, and all versions after it are also bad.

We need to find the first bad version.

## 2. Approach

I use binary search.

I have `left` and `right` to show the possible versions.

I check the middle version with `isBadVersion`.

If the middle version is bad, I know that the first bad version can be in the left part, so I move `right` to `mid`.

If the middle version is not bad, I move `left` to `mid + 1`.

I continue until `left` and `right` are the same. This is the first bad version.

## 3. Time Complexity

**O(log n)**

Every check removes about half of the possible versions, so the number of checks is logarithmic.

## 4. Space Complexity

**O(1)**

I only use a few variables like `left`, `right` and `mid`. I don't use any extra data structures.

## 5. Reflection / Improvement

Binary search is already efficient for this problem.

If I checked every version one by one, it would be `O(n)`. With binary search, it is `O(log n)`, so we need much fewer checks.
