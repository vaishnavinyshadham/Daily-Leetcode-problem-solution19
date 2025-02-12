# Daily-Leetcode-problem-solution19

PROBLEM

You are given a 0-indexed array nums consisting of positive integers. You can choose two indices i and j, such that i != j, and the sum of digits of the number nums[i] is equal to that of nums[j].
Return the maximum value of nums[i] + nums[j] that you can obtain over all possible indices i and j that satisfy the conditions.

Approach

Digit Sum Calculation: Since we need to find pairs (i, j) where the sum of digits of nums[i] and nums[j] is equal, we should calculate the sum of digits for each number.
Grouping by Digit Sum: Use a unordered_map<int, vector> where the key is the sum of digits and the value is a list of numbers having that sum.
Finding Maximum Sum: For each group, consider the two largest numbers and compute their sum. The highest sum among all groups is the answer.
Compute the sum of digits for each number.
Group numbers with the same digit sum using a hash map.
Sort each group in descending order and take the top two largest numbers to compute the max sum.
Return the maximum possible sum found.

Complexity

Time complexity:
Calculating digit sum for each number:
O(N)
Sorting groups in the worst case:
O(NlogN)
Overall complexity:
O(NlogN)

Space complexity:
O(U) (where U is the number of unique digit sums, typically much smaller than N).

 
