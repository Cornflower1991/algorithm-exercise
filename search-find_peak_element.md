# Find Peak Element

Question: [(75) Find Peak Element](http://www.lintcode.com/en/problem/find-peak-element/)

```
There is an integer array which has the following features:

    * The numbers in adjacent positions are different.

    * A[0] < A[1] && A[A.length - 2] > A[A.length - 1].

We define a position P is a peek if A[P] > A[P-1] && A[P] > A[P+1].

Find a peak element in this array. Return the index of the peak.

Note
The array may contains multiple peeks, find any of them.

Example
[1, 2, 1, 3, 4, 5, 7, 6]

return index 1 (which is number 2)  or 6 (which is number 7)

Challenge
Time complexity O(logN)
```

题解：

由时间复杂度的暗示可知应使用二分搜索。首先分析若使用传统的二分搜索，若`A[mid - 1] < A[mid] < A[mid + 1]`，则