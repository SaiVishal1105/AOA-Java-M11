
# EX 1B Power of 2
## DATE: 14-08-2025
## AIM:
To write a Java program to for given constraints.Given an integer n, return true if it is a power of two. Otherwise, return false.

An integer n is a power of two, if there exists an integer x such that n == 2x.

## Algorithm: 

1. Read an integer n from the user.

2. Check if n ≤ 0 — if true, return false (since powers of two are positive).
   
3. Use the bitwise expression (n & (n - 1)) == 0 to test if n is a power of two.
   
4. Return true if the condition holds; otherwise, false.

5. Print the result indicating whether the given number is a power of two. 

## Program:
```
Developed by: SAI VISHAL D
Register Number: 212223230180

import java.util.Scanner;

public class Solution {

    public boolean isPowerOfTwo(int n) {
     if(n<=0)
     return false;
     return(n&(n-1))==0;
     
     
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Solution sol = new Solution();
        int n = scanner.nextInt();

        boolean result = sol.isPowerOfTwo(n);
        System.out.println(result);

        scanner.close();
    }
}

```

## Output:

<img width="423" height="222" alt="image" src="https://github.com/user-attachments/assets/d9edacd9-cf32-4f85-9d91-2f71e5c4a1fa" />


## Result:
The program successfully implemented and the expected output is verified.
