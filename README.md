Remove Duplicates from Sorted Array - LeetCode Problem
Problem Description
Given a sorted array nums, remove the duplicates in-place such that each element appears only once and returns the new length.

Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory.

Example:

vbnet
Copy code
Input: nums = [1,1,2]
Output: 2, nums = [1,2]
Explanation: Your function should return length = 2, with the first two elements of nums being 1 and 2 respectively. It doesn't matter what you leave beyond the returned length.
Approach
We can use a two-pointer approach to solve this problem. We'll maintain two pointers, i and j, where i represents the current position and j represents the next position to be checked.

Initialize i to 0 (as the first element is always unique).
Iterate through the array starting from the second element.
If nums[i] is equal to nums[j], increment j to move to the next element.
If nums[i] is not equal to nums[j], increment i and update nums[i] with nums[j].
Continue this process until j reaches the end of the array.
The length of the unique elements will be i + 1, as i is 0-based.

Usage
python
Copy code
# Example Usage
nums = [1, 1, 2]
result = remove_duplicates(nums)
print(f"New length: {result}, Modified array: {nums[:result]}")
Complexity Analysis
The time complexity for this approach is O(n), where n is the length of the input array. This is because we iterate through the array only once. The space complexity is O(1) as we do not use any extra data structures.

Feel free to customize this README file as per your needs or add more information if required.





