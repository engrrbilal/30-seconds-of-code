---
title: getDistinctArraysUnion
tags: array,intermediate
---

Combined arrays distinct values or get unions of arrays.

- Use `Array.prototype.length` to check if the .
- Use `for loop` to get the arrays from arguments and push them on declared variable unionArray.
- arguments is an Array-like object accessible inside functions that contains the values of the arguments passed to that function.
- Use `Set()` to get the unique values from the combined array that is unionArray.

```js
const getDistinctArraysUnion = (...arguments) =>
  {
    const unionArray=[]
    for (let i = 0; i < arguments.length; i++) {
		  unionArray.push(...arguments[i])
	  }
    return [...new Set([...unionArray])]
  }
```

```js
getDistinctArraysUnion([1,2,3,4],[4,5,6],[1,2,7,8]) // [1,2,3,4,5,6,7,8]
getDistinctArraysUnion([1,2,3],[1,2]) //[1,2,3]
```
