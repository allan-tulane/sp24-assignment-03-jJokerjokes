# CMPS 2200 Assignment 3
## Answers

**Name:**_________________________Charles Zhang


Place all written answers from `assignment-03.md` here for easier grading.


  1a).    start with the largest possible denomination such that $2^k <= N$, then subtract $2^k$ from $N$, repeat until $N=0$
    
  1b).    The largest denomination of a coin that is less than or equal to the remaining amount $N$. Because the denominations are powers of 2, every integer can be uniquely represented in binary form. The largest coin denomination less than or equal to 
 $N$ corresponds to the highest order '1' in the binary representation of $N$. By including this coin, we effectively remove the highest order '1' from the binary representation. This step is always part of an optimal solution because it removes the largest possible 'chunk' from $N$, reducing the problem size by the greatest amount in a single step. After taking the greedy choice, we are left with a smaller subproblem: finding the minimum number of coins that sum to the new value of $N$. This subproblem is of the same form as the original problem and is independent of the prior choices made.

  1c).    $W(n)=O(lg n)$, $S(n) = O(lg n)$


2a). If $D ={1,3,4}, N=6$, the greedy algorithm will give us 1 4-dollar coin and 2 1-dollar coins, but the optimum is 2 3-dollar coins.


2b). The optimal substructure means that the optimal solution to the problem contains the optimal solutions to the subproblems. For the coin change problem, if the optimal way to change $N$ dollars is known, then for any amount less than $N$, say $N - D_i$ where $D_i$ is the denomination of a coin, the optimal solution to make $N - D_i$ dollars is part of the optimal solution to make $N$ dollars.

To prove this, assume there is a better solution for $N$ that does not include the optimal solution for $N - D_i$. This would mean that there is a way to make change for $N$ using fewer coins than the optimal solution for $N - D_i$ plus one coin of $D_i$. But this contradicts definition of the optimal solution for $N-D_i$, which is the minimum number of coins needed. Therefore, the assumption is incorrect, and the optimal solution for $N$ must include the optimal solution for 
$N-D_i$ plus the coin $D_i$.
