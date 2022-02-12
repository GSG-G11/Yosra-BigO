# Big O Notation Exercises

### Part 1

Simplify the following big O expressions as much as possible:

1. `O(n + 10)`  \\O(n)
2. `O(100 * n)`   \\ O(n)
3. `O(25)`        \\ O(1)
4. `O(n^2 + n^3)`   \\O(n^3)
5. `O(n + n + n + n)`    \\O(n)
6. `O(1000 * log(n) + n)`  \\ O(n)
7. `O(1000 * n * log(n) + n)`  \\O(n*log(n))
8. `O(2^n + n^2)`           \\O(n^2)
9. `O(5 + 3 + 1)`            \\O(1)
10. `O(n + n^(1/2) + n^2 + n * log(n)^10)`   \\O(n^2)

### Part 2

Determine the time and space complexities for each of the following functions. If you're not sure what these functions do, copy and paste them into the console and experiment with different inputs!

```js
// 1.
//O(1)
function logUpTo(n) {
//O(1) O(n)
  for (let i = 1; i <= n; i++) {
    console.log(i); //O(1)
  }
}
// O(1+1+n+1)=O(n) ....time
//O(1) ..........space

// 2.
//O(1)
function logAtMost10(n) {
  //O(1) O(1)
  for (let i = 1; i <= Math.min(n, 10); i++) {
    console.log(i); //O(1)
  }
} 
//O(1)......time
//O(1)......space

// 3.
function logAtLeast10(n) {
  for (let i = 1; i <= Math.max(n, 10); i++) {
    console.log(i);
  }
}
//O(n)......time
//O(1)......space

// 4.
//O(1)
function onlyElementsAtEvenIndex(array) {
  //O(1) 
  let newArray = Array(Math.ceil(array.length / 2));
  //O(n)
  for (let i = 0; i < array.length; i++) {
    //O(1)
    if (i % 2 === 0) {
      //O(2)
      newArray[i / 2] = array[i];
    }
  }
  //O(1)
  return newArray;
}
//O(n)......time
//O(n)......space

// 5.
//O(1)
function subtotals(array) {
  //O(1)
  let subtotalArray = Array(array.length);
  //O(1) O(n)
  for (let i = 0; i < array.length; i++) {
    //O(1)
    let subtotal = 0;
    //O(n)
    for (let j = 0; j <= i; j++) {
      //O(1)
      subtotal += array[j];
    }
    //O(1)
    subtotalArray[i] = subtotal;
  }
  //O(1)
  return subtotalArray;
}
//O(n^2)......time
//O(n)......space
```
