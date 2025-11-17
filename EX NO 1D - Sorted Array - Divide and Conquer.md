
# EX 1D Sorted Array using Divide and Conquer Approach.
## DATE: 21-08-2025
## AIM:
To write a Java program to for given constraints.
Given two sorted arrays nums1 and nums2 of size m and n respectively, return the median of the two sorted arrays.

The overall run time complexity should be O(log (m+n)).

## Algorithm:
1. Read the sizes and elements of the two sorted arrays from the user.

2. Initialize two pointers p1 and p2 to track positions in both arrays.

3. Repeatedly pick the smaller element from the two arrays using getMin() until reaching the middle position.

4. If the total length is even, compute the median as the average of the last two picked elements; otherwise, take the middle element directly.

5. Display the calculated median as the final result.


## Program:
```
Developed by: SAI VISHAL D
Register Number: 212223230180


import java.util.Scanner;

public class Solution {
    private int p1 = 0, p2 = 0;

    // Get the smaller value between nums1[p1] and nums2[p2], and move the pointer forward
    private int getMin(int[] nums1, int[] nums2) {
        if (p1 < nums1.length && p2 < nums2.length) {
            return nums1[p1] < nums2[p2] ? nums1[p1++] : nums2[p2++];
        } else if (p1 < nums1.length) {
            return nums1[p1++];
        } else if (p2 < nums2.length) {
            return nums2[p2++];
        }
        return -1; // Should not reach here if input is valid
    }

    // Main logic to find median of two sorted arrays
    public double findMedianSortedArrays(int[] nums1, int[] nums2) {
        int totalLength = nums1.length + nums2.length;
        int mid = totalLength / 2;
        int prev = 0, curr = 0;

        for (int i = 0; i <= mid; i++) {
            prev = curr;
            curr = getMin(nums1, nums2);
        }

        if (totalLength % 2 == 0) {
            return (prev + curr) / 2.0;
        } else {
            return curr;
        }    }

    // Main method with user input
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Solution sol = new Solution();

        // Input for nums1
        int m = sc.nextInt();
        int[] nums1 = new int[m];
        for (int i = 0; i < m; i++) {
            nums1[i] = sc.nextInt();
        }

        // Input for nums2
        int n = sc.nextInt();
        int[] nums2 = new int[n];
        for (int i = 0; i < n; i++) {
            nums2[i] = sc.nextInt();
        }

        // Find and display the median
        double median = sol.findMedianSortedArrays(nums1, nums2);
        System.out.println("Median of the two sorted arrays = " + median);
        
        sc.close();
    }
}

```

## Output:

<img width="1042" height="372" alt="image" src="https://github.com/user-attachments/assets/79665a41-eb35-4929-a4e3-2dee98dd8014" />




## Result:
The program successfully implemented and the expected output is verified.
