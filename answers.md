# CMPS 2200 Assignment 3
## Answers

**Name:**_________________________Charles Zhang


Place all written answers from `assignment-03.md` here for easier grading.

1.
  a. start with the largest possible denomination such that $2^k <= N$, then subtract $2^k$ from $N$, repeat until $N=0$
    
  b. The largest denomination of a coin that is less than or equal to the remaining amount $N$. Because the denominations are powers of 2, every integer can be uniquely represented in binary form. The largest coin denomination less than or equal to 
 $N$ corresponds to the highest order '1' in the binary representation of $N$. By including this coin, we effectively remove the highest order '1' from the binary representation. This step is always part of an optimal solution because it removes the largest possible 'chunk' from $N$, reducing the problem size by the greatest amount in a single step. After taking the greedy choice, we are left with a smaller subproblem: finding the minimum number of coins that sum to the new value of $N$. This subproblem is of the same form as the original problem and is independent of the prior choices made.

  c. $W(n)=O(lg n)$, $S(n) = O(lg n)$
