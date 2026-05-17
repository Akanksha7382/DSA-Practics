# ✅ Maximum Subarray 
## 🧠 Problem Statement
Given an integer array, find the contiguous subarray (subarray elements must be together) that has the largest sum, and return that sum.
Input:  [-2,1,-3,4,-1,2,1,-5,4]
Output: 6

## Solution 
## Method 1:(Kadane’s Algorithm)
### In Python
```
Input = [-2, 1, -3, 4, -1, 2, 1, -5, 4]
current_sum=0
max_sum=0

for num in Input:
    current_sum+=num
    if current_sum>max_sum:
        max_sum=current_sum
    if current_sum<0:
        current_sum=0

print(max_sum)

```
## In Js
```
let Input = [-2, 1, -3, 4, -1, 2, 1, -5, 4];
let currentSum = 0;
let maxSum = Input[0];
for (let num of Input) {
  currentSum += num;

  if (currentSum > maxSum) {
    maxSum = currentSum;
  }
  if (currentSum < 0) {
    currentSum = 0;
  }
}
console.log(maxSum);

```

## Method 2:Brute Force
- Time complexity:O(N(N+1)/2)
- space complexity :O(1)
  ### Using Python
```
Input = [-2, 1, -3, 4, -1, 2, 1, -5, 4]
current_sum=0
max_sum=0 

for i in range(len(Input)):
    current_sum=0
    for j in range(i,len(Input)):
        current_sum=current_sum+Input[j]
        max_sum=max(max_sum,current_sum)
print(max_sum)

```

### Using JS
```
let Input = [-2, 1, -3, 4, -1, 2, 1, -5, 4];
let current_sum = 0;
let max_sum = 0;

for (let i = 0; i < Input.length; i++) {
  current_sum = 0;
  for (let j = i; j < Input.length; j++) {
    current_sum = current_sum + Input[j];
    max_sum = Math.max(max_sum, current_sum);
  }
}
console.log(max_sum);

```
