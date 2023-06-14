## Mergesort
### ⭐️ Key Idea
If the left array and right array are sorted lists of length n, then we can merge them into sorted list A of length 2n in time C<sub>n</sub>

1. Split array 
2. Recursively sort both halves 
3. Merge

Merging two sorted lists is faster than sorting from scratch. 

#### Example
L : 3, 11, 28, 42 

R: 2, 8, 15, 17 

A: 2, 3, 8, 11, ... 

Both arrays, L and R, are sorted. 
All of A ≤ all of L + R

### 👾 Mergesort Pseudocode 
Mergesort(A): <br>
&emsp;&emsp;If (n=1) : Return A <br>
&emsp;&emsp;Let m ← ⎡n/2⎤ <br>
&emsp;&emsp;Let L ← A⎡1:m⎤ <br>
&emsp;&emsp;&emsp;&ensp;R ← A⎡m+1:n⎤ <br>
&emsp;&emsp;Let L ← Mergesort(L) <br>
&emsp;&emsp;Let R ← Mergesort(R) <br>
&emsp;&emsp;Let A ← Merge(A) <br>
&emsp;&emsp;Return A

### ✅️ Correctness of Mergesort
#### Induction Sketch 
At the start of iteration i:
- We have i = j + k - 1, <br>
&emsp;&emsp;&emsp;&emsp; j ≤ len(L) + 1 <br>
&emsp;&emsp;&emsp;&emsp; k ≤ len(R) + 1
- Subarray A[1..i-1] & R[1..k-1] is sorted order
- Every element in L[j..] and R[k..] is ≥ every element in A[1..i-1]

'j', 'k', and 'i' are variables that represent indices or positions in the arrays being merged.<br>
'i' represents the position in the merged array where elements from both the left (L) and right (R) subarrays are being placed. <br>
Every element in the remaining portion of the left subarray (L[j..]) and the remaining portion of the right subarray (R[k..]) is greater than or equal to every element in the merged array up to index 'i-1'. 


#### Claim 
The algorithm mergesort is correct.
- Argue that merge works. If L, R are sorted lists then Merge(L,R) are sorted
- Prove that mergesort works. For every list A, Mergesort(A) returns A in sorted order. 

#### Statement 
For every n ∈ ℕ, for every list A of size n, Mergesort(A) works.

#### Inductive Hypothesis
H(n) : For every list A of size ≤ n, Mergesort(A) works.

#### Base Case
H(1) is true "obviously"<br>
n = 1, List of length 1 is alwyas sorted.

##### Another Case
- Consider the case where j > len(L). It implies that the index 'j' has exceeded the valid range of indices for the left subarray L. It means that all elements from the left subarray have already been merged into the merged array. 
- k continues to increase because there are still elements in R. The variable i also increases accordingly based on the equation i = j + k - 1. 
- "a" mentioned in the sketch (Subarray A[1..i-1] & R[1..k-1] is in sorted order) still holds true because only elements from the right subarray R are being considered and merged with the sorted subarray A[1..i-1]. This ensures that the sorted order is maintained.

#### Inductive Step
- Assume true: ∀n, H(n) for all n < k
- Prove: H(n+1), n = k > 1
- Let A be a list of size k + 1.
- L, R are divided into sublists of size approximately k/2.
- Apply the merge sort algorithm to sort the two subarrays.
- L = Mergesort(L) is sorted, R = Mergesort(R) is sorted. We know by inductive hypothesis that the merge sort algorithm correctly sorts arrays of sizes smaller than k.
- Merge L and R together to obtain the final sorted array of size k + 1. 
- A = Mergesort(L, R) is sorted.
 
### 🏃 Runtime of Mergesort
T(n) : the running time on inputs of size n. The time depends on the input.

T(n) = 2 ᐧ T(⎡n/2⎤) + C<sub>n</sub> <br>
Size: n/2^i <br>
Work @ level i: 2^i (cn/2^i) = cn <br>
Last level: n/2^i ⇒ i = log2n <br>
Runtime: cnlog2(2n)

