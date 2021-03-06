---
layout: post
title: Tìm hiểu thuật toán Insertion Sort
categories: [algorithm]
tags: [algorithm, sort]
usejs: insertion-sort
---

### Bài toán

Cho một mảng A, sắp xếp theo thứ tự không giảm (nondecreasing).

### Mã giả

```
var A: array;
    i, j: int;

for j := 1; j < A.length; j := j + 1
    i := j - 1;
    val := A[j];

    // Chèn A[j] vào mảng A[1..j - 1]
    while (i >= 0 and A[i] > val)
        A[i + 1] := A[i];
        i := i - 1;

    A[i + 1] := val;
```

### Implement

{% highlight js linenos %}
let arr = [5, 2, 4, 6, 1, 3];
console.log('Input:', arr);     // Input: [ 5, 2, 4, 6, 1, 3 ]

for (let j = 1; j < arr.length; j++) {
    let val = arr[j];
    let i = j - 1;

    while (i >= 0 && arr[i] > val) {
        arr[i + 1] = arr[i];
        i--;
    }
    arr[i + 1] = val;
}

console.log('Output:', arr);    // Output: [ 1, 2, 3, 4, 5, 6 ]
{% endhighlight %}

Cách làm việc của thuật toán.

<div class="text-center overflow-auto">
    <canvas id="exp-canvas" width="600" height="430"></canvas>
</div>
