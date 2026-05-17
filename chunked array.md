# Problem
Given an array arr and a chunk size size, return a chunked array.

A chunked array contains the original elements in arr, but consists of subarrays each of length size. The length of the last subarray may be less than size if arr.length is not evenly divisible by size.

Please solve it without using lodash's _.chunk function.

## Example 1:
```
Input: arr = [1,2,3,4,5], size = 1
Output: [[1],[2],[3],[4],[5]]
Explanation: The arr has been split into subarrays each with 1 element.
```

## Solution
## Using Python
```
arr = [1,2,3,4,5]
size = 2
result=[]
for i in range(0, len(arr), size): 
    result.append(arr[i:i + size]) 

print(result)

```

## Using Js
```
let arr = [1,2,3,4,5]
let size = 2
let result=[]

for (let i = 0; i < arr.length; i += size) {
        result.push(arr.slice(i, i + size));
}
console.log(result);
```
