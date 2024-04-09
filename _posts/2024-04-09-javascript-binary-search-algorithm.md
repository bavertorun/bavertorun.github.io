---
layout: post
title: "JavaScript Binary Seacrh Algorithm"
tags: [JavaScript,Algorithm]
comments: true
---
Binary search algorithm is a highly efficient method used to locate a target value within a sorted array or list. It operates by continually dividing the search interval in half until the target is found or the interval becomes empty. Beginning with the entire array, the algorithm compares the target value with the middle element. If they match, the index of the target is returned. If the target is less than the middle element, the right half of the array is discarded and the search continues on the left half. Conversely, if the target is greater, the left half is discarded and the search proceeds on the right half. This process is repeated until the target is located or the search interval becomes empty. With a time complexity of O(log n), binary search is notably efficient for large datasets, although it requires the array or list to be sorted beforehand.

```
const shortedArr = [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20]

function BinarySearch(arr,target) {
    let left = 0;
    let right = arr.length-1;

    while (left <= right) {
        const mid = Math.floor((left + right) / 2)
        if(arr[mid] === target){
            return mid
        }else if(arr[mid] < target){
            left = mid+1
        }else{
            right = mid-1
        }
    }
    return -1
}

console.log(BinarySearch(shortedArr,7)) // 6
console.log(BinarySearch(shortedArr,23)) // -1

```
