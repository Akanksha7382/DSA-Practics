# Max Consecutive Ones

Given a binary array nums, return the maximum number of consecutive 1's in the array.

### Example 1:
```
Input: nums = [1,1,0,1,1,1]
Output: 3
Explanation: The first two digits or the last three digits are consecutive 1s. The maximum number of consecutive 1s is 3.
```

## Solution
### Using Python
```
arr=[0,1,1,0,0,1,1,1,1]
maxnumber=0
count=0
for i in range(len(arr)):
    if arr[i]==1:
        count+=1
    else:
        maxnumber=max(maxnumber,count)
        count=0
   
    
        
print(max((maxnumber,count)))
```
### Using Js
```
let arr = [0, 1, 1, 0, 0, 1, 1, 1, 1];
let maxnumber = 0;
let count = 0;
for (let i = 0; i < arr.length; i++) {
  if (arr[i] === 1) {
    count++;
  } else {
    maxnumber = Math.max(maxnumber, count);
    count = 0;
  }
}

console.log(Math.max(maxnumber, count));

```
