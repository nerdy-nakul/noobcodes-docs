---
sidebar_position: 71
tags: [LinkedIn]
---

# Same Tree

### Problem Statement

Given the roots of two binary trees p and q, write a function to check if they are the same or not.

Two binary trees are considered the same if they are structurally identical, and the nodes have the same value.

[Leetcode link](https://leetcode.com/problems/same-tree)

#### Example 1:

```
Input: p = [1,2,3], q = [1,2,3]
Output: true
```

#### Example 2:

```
Input: p = [1,2], q = [1,null,2]
Output: false
```

#### Example 3:

```
Input: p = [1,2,1], q = [1,1,2]
Output: false
```

#### Constraints:

- The number of nodes in both trees is in the range [0, 100].
- -10<sup>4</sup> <= Node.val <= 10<sup>4</sup>

### Code

```python title="Python Code"
class Solution:
    def isSameTree(self, p, q):
        if p is None and q is None:
            return True
        if p is None or q is None:
            return False
        return (p.val == q.val) and self.isSameTree(p.left,q.left) and self.isSameTree(p.right,q.right)

```
