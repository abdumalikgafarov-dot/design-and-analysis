# Binary Search

## 1. Problem

We have a sorted array and a target number. We need to find the index of the target. If the target is not in the array, we return `-1`.

## 2. Approach

I use binary search. First, I have `left` at the beginning and `right` at the end of the array.

Then I find the middle element.

If the middle element is equal to the target, I return its index.

If the middle element is smaller than the target, I move `left` to the right side.

If the middle element is bigger, I move `right` to the left side.

I repeat this until I find the target or `left` becomes bigger than `right`.

## 3. Time Complexity

**O(log n)**

Every time I check the middle, I remove about half of the array from the search. So I don't need to check every element.

## 4. Space Complexity

**O(1)**

I only use `left`, `right` and `mid`. I don't create any extra array.

## 5. Reflection / Improvement

Binary search is already a good solution for this problem. A simple loop through all elements would be `O(n)`, but binary search is `O(log n)`.
