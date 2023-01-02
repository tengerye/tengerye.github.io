# Common tricks of algorithms in Leetcode

## Prefix Sum
Other resouces: 

[blog](https://lfool.github.io/LFool-Notes/algorithm/%E5%89%8D%E7%BC%80%E5%92%8C%E6%95%B0%E7%BB%84.html)
### Range Sum
The questions can be converted to getting the sums of all ranges. There are three constrains: subarray (the range is continuous); the array is immutable; and we need all (or nearly all) sums of ranges.

When it is required to get maximum, minimum, count (under some constrains), we need to iterate all.

Questions can use: [304](https://leetcode.com/problems/range-sum-query-2d-immutable/), [523](https://leetcode.com/problems/continuous-subarray-sum/), [525](https://leetcode.com/problems/contiguous-array/),[560](https://leetcode.com/problems/subarray-sum-equals-k/), [2381](https://leetcode.com/problems/shifting-letters-ii/).

Questions can not use:

[307](https://leetcode.com/problems/range-sum-query-mutable/): array is mutable.

[327](https://leetcode.com/problems/count-of-range-sum/),[907](https://leetcode.com/problems/sum-of-subarray-minimums/): after applying prefix sum, we still need to iterate all combinations.


## Sliding Window
[滑动窗口](https://lfool.github.io/LFool-Notes/algorithm/%E6%BB%91%E5%8A%A8%E7%AA%97%E5%8F%A3.html), [子数组之滑动窗口篇](https://lfool.github.io/LFool-Notes/algorithm/%E5%AD%90%E6%95%B0%E7%BB%84%E4%B9%8B%E6%BB%91%E5%8A%A8%E7%AA%97%E5%8F%A3%E7%AF%87.html)

We need to iterate all subarrays where the array is immutable. Based on the constrains, we can determine whether the sliding windows (subarray which is continuous) should expand or contract. In other words, we could determine if an subarray is valid based on the previous subarray and the new element.

Good questions:
[2401](https://leetcode.com/problems/longest-nice-subarray/), [2398](https://leetcode.com/problems/maximum-number-of-robots-within-budget/), [2411](https://leetcode.com/problems/smallest-subarrays-with-maximum-bitwise-or/).

When we need to count the number of all good subarrays, we can fix the end.
[2444](https://leetcode.com/problems/count-subarrays-with-fixed-bounds/).


## Linked List
### Singly Linked List
For both adding nodes and deleting nodes, we need to get the previous node. When perform add operation, take care if add to the head. For delete, take care if the linked list is empty and if delete the head.


## Bit Operations
Is n the power of 2?  n & (n-1) == 0
Number of ones in binary representation? n.bit_count()


## Tree
### Segment Tree
The segment tree provides query and modification for the segments (continuous arrays) with time complexity of O(nlgn).
[Segment Tree](https://lfool.github.io/LFool-Notes/algorithm/%E7%BA%BF%E6%AE%B5%E6%A0%91%E8%AF%A6%E8%A7%A3.html): use global attribute (segment) to replace attributes of each item.

### Binary Tree
Usually, we need to consider how to traverse the tree and what operations shall we do during traversal.
Good questions:


### TRIE (Prefix Tree)
Given there are so many words (n) and average word length is m, if n >> m, then we could consider TRIE tree to replace n with m in complexity. It has `add(self, word: str)` and `search(self, word: str) -> bool`.


## Stack
### Monotonic Stack
The monotonic stack is mainly to solve the previous/next smaller/larger problem in linear time.
[blog1](https://itnext.io/monotonic-stack-identify-pattern-3da2d491a61e)
## Graph

<!-- ### Traversal -->
[Traversal](https://lfool.github.io/LFool-Notes/algorithm/%E5%9B%BE%E7%9A%84%E9%81%8D%E5%8E%86.html): [797](https://leetcode.com/problems/all-paths-from-source-to-target/discuss/986429/Python-Iterative-DFS-with-detailed-time-complexity-and-visuals)

[Loop test and Topological ranking](https://lfool.github.io/LFool-Notes/algorithm/%E7%8E%AF%E6%A3%80%E6%B5%8B-%E6%8B%93%E6%89%91%E6%8E%92%E5%BA%8F.html)。建议直接看算法导论。

<!-- ### Union-Find -->
[LeetCode Union find tutorial](https://leetcode.com/explore/learn/card/graph/618/disjoint-set/3844/).

## Number theory
[求素数的三种方法](https://lfool.github.io/LFool-Notes/algorithm/%E6%B1%82%E7%B4%A0%E6%95%B0%E7%9A%84%E4%B8%89%E7%A7%8D%E6%96%B9%E6%B3%95.html), [Sieve of Eratosthenes](https://cp-algorithms.com/algebra/sieve-of-eratosthenes.html), [Linear Sieve](https://cp-algorithms.com/algebra/prime-sieve-linear.html).


## Brute-force
Backtrack: use `if` statement instead of states for edge cases.


## Dyanmic Programming
### Pruning
1. Check if we can exclude impossible candidates with little cost.
2. Minimize the search space. For example, search from the end if end has fewer possibilities.

Examples:
[Word Search](https://leetcode.com/problems/word-search/).


# Other tricks
## Ceiling
To get `math.ceil(n/m)`, we can use `(n+m-1)//m`.