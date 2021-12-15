# Week 1 Sequences

This week mainly deels with arrays and strings. I want to focus on actually testing the coding that I write instead of relying on leetcode to 'test' it for me.

## Leet Code Problems

- [Two Sum](https://leetcode.com/problems/two-sum/)

- [Contains Duplicate](https://leetcode.com/problems/contains-duplicate/)
- [Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)
- [Valid Anagram](https://leetcode.com/problems/valid-anagram/)
- [Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- [Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- [Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- [3Sum](https://leetcode.com/problems/3sum/)
- [Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- [Group Anagrams](https://leetcode.com/problems/group-anagrams/)

## Notes/Solutions

[Two Sum](https://leetcode.com/problems/two-sum/)

```
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
var twoSum = function(nums, target) {
    for(let i = 0; i < nums.length; i++)
    {
        for(let j = i + 1; j < nums.length; j++)
        {
            if(nums[i] + nums[j] ==  target){
                return [i,j]
            }
        }
    }
};
```