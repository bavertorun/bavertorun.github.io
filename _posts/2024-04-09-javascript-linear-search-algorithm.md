---
layout: post
title: "JavaScript Linear Seacrh Algorithm"
tags: [JavaScript,Algorithm]
comments: true
---
Linear Search Algorithm is a simple algorithm used to determine whether a data exists within an array. The algorithm compares the searched data with each term in the array, starting from the first element to the last. If the algorithm finds a term in the array that is equal to the searched data, it returns its index. If it cannot find a term equal to the searched data, it returns -1. When it returns -1, it means that the searched item is not in the array. Since the algorithm sequentially compares the terms of the array with the searched item, it is also referred to as the linear search algorithm.
```
const arr =  [1,23,546,234,2,56,98,34,-21,31]

function LinearSeacrh(arr,element){
    const len = arr.length
    for (let i = 0; i < len; i++){
        if(arr[i] === element){
            return i
        }        
    }
    return -1
}


console.log(LinearSeacrh(arr,98)) // 6
console.log(LinearSeacrh(arr,221)) // -1

```
