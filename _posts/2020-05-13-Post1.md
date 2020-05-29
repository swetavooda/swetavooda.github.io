---
title: Jump Search
author: Sweta Vooda
date: 2020-05-29 11:33:00 +0800
categories: [Algorithms]
tags: [algorithms,searching,search-algorithm]

---

Jump search algorithm is also known as block search.
Like binary search Jump search algorithm is for sorted arrays (i.e, an interpolation searching method).
The idea of Jump search is to perform linear search on fewer elements by jumping a fixed number of steps(skipping elements) instead of searching all the elements.

For example:

`arr={0,0,9,11,14,17,22,29,40,68,110,112,212,222,490,700};`

has 16 elements so assuming block size to jump is **4** and element to search is **110**

Step 1: Jump from index 0-3

Step 2: Jump from index 4-7

Step 3: Jump from index 8-11

Step 4: Since element at index 12 is larger that 110 go back and perform linear search on (indexes 8-11).


### Optimal block size

the optimal block size is  **√n**  for minimum Time complexity

### Time complexity

Worst case time complexity: `O(√N)`

Average case time complexity: `O(√N)`

Best case time complexity: `O(1)`


### Space complexity 
`O(1)`

### Points to remember
* Jump search is used only for sorted data.
* It is slower than Binary search.

## When to use Jump search
Jump search only needs to jump backwards once, while a binary can jump backwards up to log(n) times. This can be important if a jumping backwards takes significantly more time than jumping forward.

Example: while searching for data stored on physical drives with spinning mediums it is very expensive to move back and forth.

*The use case for jump search (O(√n)) over binary search (O(log n)) is when jumping back is expensive.*



**Find the Implementation of Jump Search Algorithm** [here](https://github.com/swetavooda/Algorithms/blob/master/JumpSearch.java){:target="_blank"}.