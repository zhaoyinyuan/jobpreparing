链表中倒数第k个结点

时间限制：1秒 空间限制：32768K 

本题知识点： [链表](https://www.nowcoder.com/questionCenter?questionTypes=000100&mutiTagIds=580)

## 题目描述

输入一个链表，输出该链表中倒数第k个结点。

**遍历整个链表，之后计算链表长度，再这个基础上正着再遍历一次，注意没有这么多结点的情况如何处理**

```python
# -*- coding:utf-8 -*-
class ListNode:
    def __init__(self, x):
        self.val = x
        self.next = None

class Solution:
    def FindKthToTail(self, head, k):
        # write code here
        n = 0
        p = head
        while p != None:
            n += 1
            p = p.next
        if n<k:
            return None
        p = head
        m = 1
        while m < (n-k+1):
            m += 1
            p = p.next
        return p
```

