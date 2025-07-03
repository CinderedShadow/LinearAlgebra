The project we made is called 112tor41, which teaches 21-241 concepts using 15-112 programming. We made a library with many functions, without utilizing linear algebra external modules like numpy. The library carries out operations and analyzes the properties of matrices (2D lists) and vectors (1D lists).

Our project includes the following features as functions:
  - prettyMatrix(matrix): Rounds all floating point entries to the nearest tenth decimal place and converts entries ending with .0 to integers.
  - transpose(matrix): Returns the transpose of a matrix (matrix with rows as columns and columns as rows).
  - determinant(matrix): Calculating the determinant of any sized square matrix using recursion.
  - isEchelonForm(matrix): Checks if the given matrix is in echelon form
  - getEchelonForm(matrix) and getReducedEchelonForm(matrix): Finding the echelon and reduced echelon forms of a matrix using Gaussian Elimination.
  - generateMatrix(rows, cols), generateSquareMatrix(n): Generating matrices and square matrices of random sizes with random entries.
  - getIdentityMatrix(n): Returns the n by n identity matrix (diagonal entries = 1, rest of entries = 0).
  - getInverse(matrix): Uses a cofactorMatrix(matrix) function.
  - getNullSpace(matrix): Finds the null space of a matrix.
  - getColumnSpace(matrix): Finds the column space of a matrix
  - dotProduct(v1, v2): Returns the dot product of two vectors.
  - norm(v): Returns the norm of a vector, which is the square root of dotProduct(v, v).
  - isOrthogonal(v1, v2): Returns if two vectors are orthogonal (dot product = 0).
  - isOrthonormal(v1, v2): Returns if two vectors are orthonormal (orthogonal and the norm of each vector = 1).
  - isSquare(matrix): Returns if a matrix is square (same amount of rows and columns).
  - isIsometry(matrix): Returns if a matrix is an isometry.
  - getEigenvalues(EF): Finds the eigenvalues of a matrix by converting into echelon form getting the diagonals. Returns a dictionary with eigenvalues as keys and algebraic multiplicity as corresponding values.
  - rowReplacement(matrix, (row1, row2), OptionalScaling): Adds row1 to row2 after scaling it if provided
  - getRowReplacementMatrix(matrix, (row1, row2), OptionalScaling): Gets the elementary matrix which can perform desired row ereplacement
  - rowExchange(matrix, (row1, row2)): Swaps row1 and row2
  - getRowExchangeMatrix(matrix, (row1, row2)): Gets the elementary matrix which can swap row1 and row2.
  - rowScaling(matrix, (scale, row)): Multiplies the given row by the scale
  - getRowScalingMatrix(matrix, (scale, row)): Gets the elementary matrix which can perform row scaling
  - getMatrixSolution(A,b): Takes a matrix A and a column vector b and returns the solution of Ax=b (including infinite solution case), or returns None if it doesn't exist.

The functions have appropriate conditions that check if it is possible to carry out the specific operations. For example, the getInverse function first checks if the determinant of the matrix is not zero (otherwise, there would be a ZeroDivisionError).
  
We also created a draft of a potential educational game that can be made, with descriptions of linear algebra concepts and interactive quizzes. The game first asks if the user is ready to begin. Once the user inputs a string containing 'yes', Section 1: Introduction is presented. Then, the game asks the user if they want to continue. Once the user inputs a string containing 'yes', then they are presented with a quiz. The quiz generates a 2x2 square matrix with random entries and asked to determine the determinant of the matrix. They can continue when they have found the correct determinant of a matrix correctly. 

Fun Fact: We found typos in our professor's 241 lecture notes using our code. :)