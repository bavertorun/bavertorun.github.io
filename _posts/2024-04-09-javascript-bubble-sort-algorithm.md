---
layout: post
title: "JavaScript Bubble Sort Algorithm"
tags: [JavaScript, Algorithm]
comments: true
---
Bubble Sort is a sorting algorithm that iterates over a list, comparing adjacent elements and swapping them if they are in the wrong order. This process continues until the list is sorted. Each iteration "bubbles" the largest (or smallest) element to its correct position. The algorithm's time complexity is O(n^2), making it inefficient for large datasets compared to other sorting algorithms such as Quick Sort or Merge Sort. However, it can be useful for educational purposes or sorting small datasets.
```
let arr = [1, 32, 45, 2, 5, 78, 3, 23];

function BubbleSort(arr) {
  const len = arr.length;

  for (let i = 0; i < len; i++) {
    for (let j = 0; j < len-i; j++){
           if(arr[j] > arr[j+1]){
                let temp = arr[j]
                arr[j] = arr[j+1]
               arr[j+1] = temp
           }
        }
    }
    return arr
}

console.log(BubbleSort(arr)) // [1,  2,  3,  5, 23, 32, 45, 78]
```
