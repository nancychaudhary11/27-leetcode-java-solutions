# LeetCode 27 - Remove Element

## Problem

Given an integer array `nums` and an integer `val`, remove all occurrences of `val` in-place and return the number of remaining elements.

## Approach

This solution uses the **Two Pointers** approach.

- `i` scans every element of the array.
- `k` keeps track of where to place the next valid element.
- Elements that are not equal to `val` are copied to the front of the array.

## Java Solution

```java
class Solution {
    public int removeElement(int[] nums, int val) {
        int k = 0;

        for (int i = 0; i < nums.length; i++) {
            if (nums[i] != val) {
                nums[k] = nums[i];
                k++;
            }
        }

        return k;
    }
}
```

## Example

**Input:**
```text
nums = [3,2,2,3]
val = 3
```

**Output:**
```text
2
```

The first two positions of the modified array contain:

```text
[2,2]
```

## Complexity

- Time Complexity: O(n)
- Space Complexity: O(1)

## LeetCode Problem

Problem Number: 27  
Problem Name: Remove Element
