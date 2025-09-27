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
