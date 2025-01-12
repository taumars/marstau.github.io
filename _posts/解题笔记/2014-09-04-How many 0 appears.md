---
layout: post
title: How many 0 appears
category: 数据结构与算法
tags: data　structure／algorithm
keywords: 
description: 
---

**<span
style="color:#e53333;">How many 0 appears in 0,1,2,3,...,999,1000?</span>**

**<span style="color:#e53333;">A 189</span>**

**<span style="color:#e53333;">B 191</span>**

**<span style="color:#e53333;">C 193</span>**

**<span style="color:#e53333;">D </span><span
style="color:#e53333;">195</span>**

解析:

**方法1:**

数字比较小,可以直接求。

0\~9 —— 1

10\~99 —— 9

100\~199 —— 20

200\~299 —— 20

...

900\~999 —— 20\
 1000 —— 3

相加得:1 + 9 + 20\*9 + 3 = 193.

**方法2:**

如果数字很大的话,可以考虑排列组合,

0\~9 —— 只有个位数,锁定个位数为0的情况下,只有1种情况.

10\~99 —— 锁定个位数,十位数可以为1\~9这9种排列,有C(9,1) = 9.

100\~999 —— 分成三种情况:

    (1)仅个位数为0,十位数为C(9,1),百位数为C(9,1),所以为C(9,1)\*C(9,1) =
81.

    (2)仅十位数为0,个位数为C(9,1),百位数为C(9,1),所以为C(9,1)\*C(9,1) =
81.

    (3)个位数和百位数都为0, 因为每种情况都有两个0,所以要乘以2, 2\*C(9,1)
= 18.\
 相加得180种.

1000 —— 3种.

相加得:1 + 9 + 180 + 3 = 193.

 

extended:

对于求非0的个数用第二种方法可以更简单。

例如求1\~N中有多少个1.

求1000,

0\~999 —— 分成三种情况:

 (1)
仅个位数或十位数,或百位数为1,即只有1个1,个、十、百三种情况,所以3\*1\*C(9,1)\*C(9,1)
= 243.

 (2)
有两个1,有十个、百个、百十三种情况,又每种情况有两个1,所以3\*2\*C(9,1) =
54.

 (3) 有三个1.有百十个一种情况,每种情况有三个1,所以1\*3 = 3.

相加得300.

1000 —— 1.

相加得:300 + 1 = 301.







