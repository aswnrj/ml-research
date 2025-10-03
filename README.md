# ml-research
My ML/Deep Learning journey – notes + experiments

## Linear Algebra 
### Lecture 1 - The geometry of linear equations
- Row picture and column picture
- How row picture might not always be useful to visualize and find the intersecting point
- Column picture is a better representation
- Visualizes how an n n-dimensional vectors can fill the n-dimensional space if none of them are orthogonal
- If out of three vectors, two are duplicate or lie on the same line or all three lie on the same plane, the combination can fill only that plane

### Lecture 2 - Elimination using matrices
- How to solve 3 3-d equations using matrix elimination
- Multiplying a 3x3 matrix with a 3x1 vector will result in a linear commbination of cols of the matrix
- Multiplying a 1x3 vector with a 3x3 matrix will result in a linear combination of the rows of the matrix
- We need to make the matrix an upper triangular matrix in order to solve it from bottom to up
- If some pivot becomes 0, we can try to rearrange. If rearrange is not possible, then there won't be any solution
- To transform A into U, we need to multiple it by a series of matrices
- To permute a matrix, we have to multiple it by the specific permutation of the identity matrix

## Probability
### Lecture 1 - Probability Models and Axioms
- A sample space is a set of all possible outcomes
- An event is a subset of the sample space
- We can consider probability of an event happening
- 3 axioms of probability
    - Non-negativity
    - Normalization
    - Additivity
- The probability of a set of outcomes happening in a countably finite set is the sum of probabilities of each outcome
- **Discrete uniform law**: \
If all outcomes are equally likely, the probability\
$$P(A) = \frac{number\ of\ elements\ in\ A}{total\ number\ of\ elements\ in\ the\ sample\ space}$$
- **Continuous uniform law**:\
Probability = Area\
Probability of a single point = 0

### Lecture 2 - Conditioning and Bayes Theorem
- Probability of A occuring given that B has occured\
$$P(A|B) = \frac{P(A\cap B)}{P(B)}$$
- Intuitive way to think about it is that the probability of B will become 1, but the probabilities of partitions in B will remain the same
- Conditional probability follows all the properties of normal probability
- If the sample space is divided into a set of events $A_i$ and we have data about how likely if another event $B$ going to occur if each of events $A_i$ occurs, we can use this data to find the total probability of event $B$ occuring.\
$$P(B) = \sum_{i} P(A_i)\cdot P(B|A_i)$$
- This can also be used to find the inference probability to understand if $B$ has occured, what are the probabilities of it being due to each $A_i$\
$$P(A_i|B) = \frac{P(A_i)\cdot P(B|A_i)}{\sum_{j} P(A_j)\cdot P(B|A_j)}$$

## Linear Algebra
### Lecture 3 - Multiplication and Inverse Matrices
$$
A\cdot B = C
$$
- Columns of $C$ are linear combinations of columns of $A$ weighted by columns of $B$
- Rows of $C$ are linear combinations of rows of $B$ weighted by rows of $A$
- $C$ is sum of columns of $A$ multipled by rows of $B$
- A matrix is singular or non-invertible if there exists a non-zero $X$ where $A \cdot X = 0$
- Guass - Jordan method of finding inverse\
$$E [A\ I] = [I\ A^{-1}]$$

### Lexture 4 - Factorization of $A = LU$
- We can form U by doing some operations on $A$ using $E$ keeping pivot constant and converting other elements to $0$
- $L$ is the inverse of this $E$ matrix
- $L$ is a cleaner matrix than $E$ and the multipliers go directly into $L$, unlike in $E$ where the multipliers accumulate and form new numbers 
- The number of operations required to convert a $n \times n$ matrix $A$ into $U$ is of the order $\frac{n^3}{3}$
- The permutations matrices form a set of matrices where multiplication and inverses of those lie in the same set
- The number of matrices in this set for $n=3$ is $6$. Here $P^{-1} = P^{T}$

### Lecture 5 - Transposes, Permutations and $R^n$ spaces
- If we include rearranging rows also to get pivots, the equation becomes $P\cdot A = L\cdot U$
- $n \times n$ matrices have $n!$ permuations matrices
- $P^{T}\cdot P = I$ 
- For any matrix, $R^{T}R$ is a symmetric matrix
- Vector spaces are a set of vectors where all linear combinations of these vectors lie in the same vector space. 
- Subspaces of $\mathbb{R}^{2}$ are
    - Whole of $\mathbb{R}^{2}$
    - A line passing through $ \begin{bmatrix} 0 \\ 0 \end{bmatrix}$
    - Only the point $(0, 0)$
- The column space of A, $C(A)$ is the subspace of $\mathbb{R^m}$ formed by the linear combinations of all the columns of $A$

### Lecture 6 - Column spaces and Null spaces
- Column spaces are all the linear combinations of the columns of $A$
- A nullspace contains all the solutions for $A\cdot x = 0$
- Consider a $4\times 3$ matrix, the column space will be a subspace of $\mathbb{R}^4$ and the nullspace will be a subspace of $\mathbb{R}^3$
- Both column spaces and null spaces are valid vector spaces and satisfy all the properties of these
- The solutions of $A\cdot x = b$ does not form a subspace

## Probability
### Lecture 3 -  Independence
- Two events are independent if the occurence of one events does not provide any information about the occurence of the other
- $P(A | B) = P(A)$
- $P(A \cap B) = P(A) \cdot P(B)$
- Same way for multiple independent events. They are also mututally independent
- But if some events are mutually independent, that does not imply total independence
- Interesting problem about the king's sibling

## Linear Algebra 
### Lecture 7
- Rank is the number of pivots after converting $A$ to $U$
- After conversions, we can call them free columns and pivot columns
- Substitute $1$ and $0$ for the free variables and find the values of pivot variables
- The nullspace will be a linear combination of these solutions
- We can write these solutions to form a matrix whose column space will be the nullspace
- We can also see that we can divide the RREF form of the matrix into $I$ and $F$ where $F$ is the free column matrix
- $N$ will be of the form $ \begin{bmatrix} -F \\ I \end{bmatrix} $
- Rank($A$) = Rank($A^T$) 

## Probability
### Lecture 4 - Counting
- Learnt about ways to choose k from n elements and about permutations of them
- Solved a few problems
- If $n$ is partitioned into $n_1, n_2 \cdots n_k$, the ways of partitioning them is $$ \frac{n!}{n_1! \cdot n_2! \cdots n_k!} $$
