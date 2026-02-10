# 448. Find All Numbers Disappeared in an Array

##  Problem Description
Given an array `nums` of `n` integers where `nums[i]` is in the range `[1, n]`, return an array of all the integers in the range `[1, n]` that do not appear in `nums`.

**Link to Problem:** [LeetCode #448](https://leetcode.com)

---

##  Examples
**Example 1:**
- **Input:** `nums = [4,3,2,7,8,2,3,1]`
- **Output:** `[5,6]`

**Example 2:**
- **Input:** `nums = [1,1]`
- **Output:** `[2]`

---

##  Solution Approach
The problem requires finding missing values within a specific range $[1, n]$.

1. **Frequency Array:** We create an auxiliary array `freq` of size $n+1$.
2. **Counting:** Iterate through the input array and increment the index in `freq` corresponding to the value found in `nums`.
3. **Identification:** Iterate from $1$ to $n$. If `freq[i]` is $0$, it means the number $i$ never appeared in the input, so we add it to our result list.

### Complexity Analysis
- **Time Complexity:** $O(n)$ — We traverse the array twice.
- **Space Complexity:** $O(n)$ — We use an extra array of size $n$ to store frequencies.

---

