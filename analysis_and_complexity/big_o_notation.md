## Big-O Notation
### ⭐️ Asymptotic Analysis
We don't have enough information to precisely predict the running time of an 
algorithm, so we use asymptotic analysis and express the time complexity using
Big-O notation.  Big-O notation provides an upper bound on the growth rate of 
an algorithm's running time.
#### Running time may depend on:
- Input size
- The input itself
- The machine that will run the algorithm
<br>

It is impractical to precisely count operations when analyzing the running time
of an algorithm. Different factors, like the ones listed above, make it difficult to determine the exact number 
of operations performed by an algorithm.

We want to focus on the dominant factor that contributes the most to the overall 
time complexity, and that is input size. Big-O notation can be used to describe an 
algorithm's behavior as input size grows infinitely without having to take into account 
the number of operations.

### 🅾️ "Big-Oh" Notation
Describes limiting behavior of a function when the argument tends towards a particular value.
It describes the asymptotic behavior of a function.

f(n) = O(g(n)) if there exists c ∈ (0,∞) and n<sub>o</sub> ∈ ℕ such that f(n) ≤ c ᐧ g(n) for every n ≥ n<sub>o</sub>
- Asymptomatic version of: f(n) ≤ g(n)
- Roughly equivelent to: lim<sub>n → ∞</sub> f(n)/g(n) < ∞
