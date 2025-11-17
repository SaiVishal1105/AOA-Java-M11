
# EX 1A Print All Numbers 
## DATE: 11-08-2025
## AIM:
To Write a Java program that takes an integer input N from the user and prints all the numbers from 1 to N, separated by spaces, on a single line..

## Algorithm
1. Read an integer input N from the user.
2. Check if N ≤ 0 — if true, display "Invalid input. N must be greater than 0.".
3. If N > 0, initialize a loop variable i = 1.
4. Repeat the loop while i ≤ N, printing each number followed by a space.
5. Increment i after each iteration to continue the sequence.
 
## Program:
```

Developed by: SAI VISHAL D 
Register Number: 212223230180

import java.util.*;
public class demo
{
    public static void main(String args[])
    {
        Scanner s=new Scanner(System.in);
        int N,i;
        N=s.nextInt();
        if(N<=0)
        {
            System.out.println("Invalid input. N must be greater than 0.");
        }
        else
        {
            for(i=1;i<=N;i++)
            {
                System.out.print(i+" ");
            }
        }
    }
} 

```

## Output:



<img width="472" height="177" alt="image" src="https://github.com/user-attachments/assets/eb986c3a-2d46-448e-b877-b0bdeb237e72" />


## Result:
The program successfully print all the numbers from 1 to N. 
