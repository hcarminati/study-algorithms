## Mergesort
### ⭐️ Key Idea
Merging two sorted lists is faster than sorting from scratch. 

If the left array and right array are sorted lists of length n, then we can merge them into sorted list A of length 2n in time C<sub>n</sub>

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

#### Inductive Step
- Assume true: ∀n, H(n)
- Prove: H(n+1)
- Let A be a list of size n + 1.
- L, R are lists of size ≤ n
- L = Mergesort(L) is sorted, R = Mergesort(R) is sorted by inductive hypothesis
- A = Mergesort(L, R) is sorted 

### 🏃 Runtime of Mergesort
T(n) : the running time on inputs of size n. The time depends on the input.

T(n) = 2 ᐧ T(

