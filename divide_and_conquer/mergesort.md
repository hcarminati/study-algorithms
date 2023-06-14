## Mergesort
### ⭐️ Key Idea
If the left array and right array are sorted lists of length n, then we can merge them into sorted list A of length 2n in time C<sub>n</sub>

Merging two sorted lists is faster than sorting from scratch. 

#### Example
L : 3, 11, 28, 42 

R: 2, 8, 15, 17 

A: 2, 3, 8, 11, ... 

Both arrays, L and R, are sorted. 
All of A ≤ all of L + R

### ✅️ Correctness of Mergesort
#### Claim 
The algorithm mergesort is correct 
- Argue that merge works. If L, R are sorted lists then Merge(L,R) are sorted
- Prove that mergesort works. For every list A, Mergesort(A) returns A in sorted order. 

#### Statement 
For every n ∈ ℕ, for every list A of size n, Mergesort(A) works.

#### Inductive Hypothesis
H(n) : For every list A of size ≤ n, Mergesort(A) works

#### Base Case
H(1) is true "obviously"
