# Longest Subarray of Evens and Odds

![Difficulty](https://img.shields.io/badge/Difficulty-Medium-yellow)

## Problem

Given an array  **arr[],**  return the **maximum possible length** of a subarray such that its elements are arranged alternately either as even and odd or odd and even.

 **Examples:** 

```
Input: arr[] = [10, 12, 14, 7, 8]
Output: 3
Explanation: The max length of subarray is 3 and the subarray is [14, 7, 8]. Here the array starts as an even element and has odd and even elements alternately.

```

```
Input: arr[] = [4, 6]
Output: 1
Explanation: The array contains [4, 6]. So, we can only choose 1 element as that will be the max length subarray.
```

 **Constraints:** 
1 ≤ arr.size() ≤ 106
1 ≤ arr[i] ≤ 103

## Solution

**Language:** Java  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-08-01T13:03:07.063Z  

```java
class Solution {
    public static int maxEvenOdd(int arr[]) {
        //  code here
        int n=arr.length,res=1,cur=1;
        int next=(arr[0]%2==0)?1:0;
        for(int i=1;i<n;i++){
            if(arr[i]%2==next){
                cur++;
                res=Math.max(res,cur);
                next=(next==1)?0:1;
            }
            else
                cur=1;
        }
        return(res);
    }
}
```

---

[View on GeeksforGeeks](https://practice.geeksforgeeks.org/problems/longest-subarray-of-evens-and-odds/1)