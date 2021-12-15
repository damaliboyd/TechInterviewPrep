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

### [Two Sum](https://leetcode.com/problems/two-sum/)

My initial solution is a brute force attempt. It is has been a long time since my DS and Algo class so I am not too familiar with anything that could help optimize this so I am gonna check out other people answers to this.
[A Techsith video on it.](https://www.youtube.com/watch?v=_CoCO62fn_E) I think the advice on creating test cases before writing code is smart. TDD for the win. Also noted getting the length of the array and setting it to a variable instead of getting length in the for loop to reduce the time of the problem.
```
\\ My solution it passes with a time complexity of O(n^2)
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

Techsith's solution:
I am curious to see if the idea of compliments comes up in other questions.
```
var twoSum = function(nums, target) {
    const comp = new Map();
    const len = nums.length;
    
    for(let i = 0; i < len; i++){
        if(comp[nums[i]] >= 0){
            return [comp[nums[i]], i]
        }
        comp[target - nums[i]] = i;
    }
    return []
};
```

### [Contains Duplicate](https://leetcode.com/problems/contains-duplicate/)
Potential future reference: [Blind 75 Python by NeetCode](https://www.youtube.com/watch?v=KLlXCFG5TnA&list=PLot-Xpze53ldVwtstag2TL4HQhAnC8ATf)