# 数字在排序数组中出现的次数

**题目**
统计一个数字在排序数组中出现的次数。

**测试地址**
[数字在排序数组中出现的次数](https://www.nowcoder.com/practice/70610bf967994b22bb1c26f9ae901fa2?tpId=13&tqId=11190&tPage=2&rp=2&ru=/ta/coding-interviews&qru=/ta/coding-interviews/question-ranking)

## 解题思路

最容易想到的算法就是遍历一遍数组求出指定的K出现的次数。时间复杂度是o(N)，空间复杂度也是o(1)

题目给出的是排序好的数组，因此，指定的数必然是连续的出现，我们只需要找到第一次他出现的位置以及最后一次他出现的位置，然后做差即可。
对于排序数组，求出现位置，必然是二分查找，如果找到的中间值是目标值，还需要判断他前面是否有目标值，有就在前半段继续查找来得到第一次出现的位置。
对于最后出现的位置也是用这个方法得到。时间复杂度是o(lgN)