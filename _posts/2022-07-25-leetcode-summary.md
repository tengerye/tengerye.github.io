# Common tricks of algorithms in Leetcode

## Prefix Sum
Other resouces: 

[blog](https://lfool.github.io/LFool-Notes/algorithm/%E5%89%8D%E7%BC%80%E5%92%8C%E6%95%B0%E7%BB%84.html)
### Range Sum
The questions can be converted to getting the sums of all ranges. There are three constrains: subarray (the range is continuous); the array is immutable; and we need all (or nearly all) sums of ranges.

When it is required to get maximum, minimum, count (under some constrains), we need to iterate all.

Questions can use: [304](https://leetcode.com/problems/range-sum-query-2d-immutable/), [523](https://leetcode.com/problems/continuous-subarray-sum/), [525](https://leetcode.com/problems/contiguous-array/),[560](https://leetcode.com/problems/subarray-sum-equals-k/).

Questions can not use:

[307](https://leetcode.com/problems/range-sum-query-mutable/): array is mutable.

[327](https://leetcode.com/problems/count-of-range-sum/),[907](https://leetcode.com/problems/sum-of-subarray-minimums/): after applying prefix sum, we still need to iterate all combinations.


## Sliding Window
[滑动窗口](https://lfool.github.io/LFool-Notes/algorithm/%E6%BB%91%E5%8A%A8%E7%AA%97%E5%8F%A3.html), [子数组之滑动窗口篇](https://lfool.github.io/LFool-Notes/algorithm/%E5%AD%90%E6%95%B0%E7%BB%84%E4%B9%8B%E6%BB%91%E5%8A%A8%E7%AA%97%E5%8F%A3%E7%AF%87.html)

We need to iterate all subarrays where the array is immutable. Based on the constrains, we can determine whether the sliding windows (subarray which is continuous) should expand or contract. In other words, we could determine if an subarray is valid based on the previous subarray and the new element.


## Linked List
### Singly Linked List
For both adding nodes and deleting nodes, we need to get the previous node. When perform add operation, take care if add to the head. For delete, take care if the linked list is empty and if delete the head.