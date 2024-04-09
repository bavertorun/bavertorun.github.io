---
layout: post
title: "JavaScript Binary Seacrh Algorithm"
tags: [JavaScript,Algorithm]
comments: true
---
Linear Search Algorithm, bir dizide belirli bir verinin varlığını tespit etmek için kullanılan basit bir yöntemdir. Dizi içinde aranan veriyi, ilk öğeden başlayarak son öğeye kadar tek tek karşılaştırır. Eğer algoritma, aranan veriye eşit olan bir öğe bulursa, onun indisini döndürür. Eğer aranan veriyle eşleşen bir öğe bulunamazsa, -1 değerini döndürür; bu durumda aranan öğenin dizide bulunmadığı anlamına gelir. Algoritma, dizi içindeki terimleri sıralı olarak aranan öğe ile karşılaştırdığı için sıklıkla doğrusal arama algoritması veya sıralı arama algoritması olarak da adlandırılır.

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
