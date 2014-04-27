### Introduction

This pair of functions enables a user to cache the inverse of a matrix. There are two sets of functions: 
1.  `makeCacheMatrix`: This function creates a special "matrix" object
    that can cache its inverse.
2.  `cacheSolve`: This function computes the inverse of the special
    "matrix" returned by `makeCacheMatrix` above. If the inverse has
    already been calculated (and the matrix has not changed), then
    `cacheSolve` retrieves the inverse from the cache.

### Assumptions

This function makes two assumptions: 
1. A square matrix has been input into the function
2. The matrix supplied is always invertible.

### `makeCacheMatrix`:

This first function, `makeCacheMatrix` creates a special "matrix", which is
really a list containing a function to

1.  set the value of the matrix
2.  get the value of the matrix
3.  set the value of the inverse
4.  get the value of the inverse

###

The following function calculates the inverse of the special "matrix"
created with the above function. However, it first checks to see if the
inverse has already been calculated. If so, it `get`s the inverse from the
cache and skips the computation. Otherwise, it calculates the inverse of
the data and sets the value of the matrix inverse in the cache via the `setsolve`
function.