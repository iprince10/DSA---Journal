# Arrays Problems Journal

This section contains all the array problems I solve, along with short explanations of their approaches.

## 📌 Problem 1:
**LeetCode 704** - Binary Search (https://leetcode.com/problems/binary-search);
**Approach**
  - Use binary search
  - Time _O(log n ) | Space_O(1)

## 📌 Problem 2:
**LeetCode 53** - Maximum Subarray ( https://leetcode.com/problems/maximum-subarray);
**Approach**
 - Use Kadane's Algorithm :Initialize current sum and max sum, track current sum, update maxsum with max(cs,ms) ,reset cs if negative, keep max.
 - Time_O(n) | Space_O(1)

## 📌 Problem 3:
**LeetCode 121** - Best Time to buy and Sell Stock (https://leetcode.com/problems/best-time-to-buy-and-sell-stock);
**Approach**
 - Intiliaze Buyprice with initial price or +infinity and maxprofit with 0 , update buyprice if selling price is lower (b.p.= s.p.) or calculate         profit if buyprice is < selling price.
 - Then update maxprofit with max(profit, maxprofit), keep maxprofit

## 📌 Problem 4:
**LeetCode 42**-Trapping Rain Water(https://leetcode.com/problems/trapping-rain-water);
**Approach**
 - Calculate leftmaximum and rightmaximum boundary by creating leftmax and rightmax array[]. [0]th index is same , other index are max(height[i],lm[i-1];
 - Calculate waterlevel for each height[i] by min(leftmax[i],rightmax[i]).
 - Initialize trappedrainwater by 0 and calculate trw by +=waterlevel -height[i].
 - keep trappedrainwater.
   
## 📌 Problem 5:
**LeetCode 287**- Find the duplicate number (https://leetcode.com/problems/find-the-duplicate-number);
**Approach**
 - Use binary search on the value range from 1 to n.
 - For each mid, count how many numbers in the array are <= mid.
 - If count > mid, the duplicate must be in the left half; otherwise, it’s in the right half.
 - Narrow down until low == high, which is the duplicate number.

## 📌 Problem 6:
**LeetCode 136**- Single Number(https://leetcode.com/problems/single-number);
**Approach**
 - Bit Manipulation, initialize a variable index with 0 and for the array length:
 - XOR of number with itself is 0 and XOR of number with 0 is number itself, return index

## 📌 Problem 7:
**LeetCode 33**- Search in sorted rotated array(https://leetcode.com/problems/search-in-rotated-sorted-array):
**Approach**
 - Initialize start and end of the array . Calculate mid while start<end.
 - If number[mid]== target , return mid; if not check for both sorted rotated left and sorted rotated right.
 - For sorted left half, if number lies in left update end ,else start.
 - For sorted right half . if number lies in right side update start, else end .
 - Return -1 , if number not found.

## 📌 Problem 8:
**LeetCode 81**-Search in sorted rotated array ii (https://leetcode.com/problems/search-in-rotated-sorted-array-ii):
**Approach**
 - Initialize left and right of the array . Calculate mid while left <= right .
 - If number[mid]== target , return true;
 - Put condition if (nums[left]== nums[mid] && nums[right]== nums[mid]) , increment left++ decrement right -- ,continue,this cancels out repeated nums that causes problems in finding left and right sorted arrays from both sides of mid.
 - If nums [mid} != target , check for both sorted rotated left and sorted rotated right.
 - For sorted left half, if number lies in left update right ,else left.
 - For sorted right half . if number lies in right side update left, else right.
 - Return false , if number not found.

## 📌 Problem 9:
**LeetCode 560**- Subarray Sum equals k (https://leetcode.com/problems/subarray-sum-equals-k):
**Approach**
 - This approach is not optimal but still can be used , use hashmap for better solution.
 - initialise count variable as 0 and declare sum variable . Calculate sum for outer loop index and if sum == target , count++
 - similarly for inner loop starting from index+1 , do the same and return count.

## 📌 Problem 10:
**LeetCode 153**-Find minimum in rotated sorted array(https://leetcode.com/problems/find-minimum-in-rotated-sorted-array):
**Approach**
 - Use Binary search , initialize left and right (since it demands last element (left<right)not equal to.
 - calculate mid , compare mid with right , if mid >= right , update left,else right = mid .
 - Return nums[left].
