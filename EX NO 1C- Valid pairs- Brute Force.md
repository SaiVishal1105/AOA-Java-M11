
# EX 1C Valid Pairs using Brute Force Approach
## DATE: 18-08-2025
## AIM:
To write a Java program to for given constraints.
Given an integer array nums and an integer k, return the number of pairs (i, j) where i < j such that |nums[i] - nums[j]| == k.

The value of |x| is defined as:

x if x >= 0.
-x if x < 0.

## Algorithm
1. Read the array size n, elements of the array, and integer k.


2. Initialize a counter count to zero.


3. Use two nested loops to compare every unique pair of elements in the array.


4. If the absolute difference between any two elements equals k, increment count.


5. After all comparisons, print the final value of count as the result.



## Program:
```
Developed by: SAI VISHAL D
Register Number: 212223230180

import java.util.Scanner;
public class CountPairsWithDifference {
    public static int countKDifference(int[] nums, int k) {
        int count = 0;
        for(int i =0;i<nums.length;i++)
        {
            for(int j=i+1;j<nums.length;j++)
            {
                if(Math.abs(nums[i] - nums[j]) == k)
                {
                    count++;
                }
            }
}
        return count;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] nums = new int[n];
        for (int i = 0; i < n; i++) {
            nums[i] = sc.nextInt();
        }
        int k = sc.nextInt();
        int result = countKDifference(nums, k);
        System.out.println(result);
        sc.close();
    }
}

```

## Output:
<img width="485" height="323" alt="image" src="https://github.com/user-attachments/assets/b222a26a-966b-4ece-ba32-4351a8dbe786" />




## Result:
The program successfully implemented and the expected output is verified.
