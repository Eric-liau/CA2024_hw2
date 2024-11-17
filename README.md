# Assignment 2: Classify


## Functions
### abs
This function converts the input value to its absolute value. When the input value is negative, I use 0 minus the input value to implement the absolute value conversion.
### relu
This function converts every element x in input array to max(x,0).
### argmax
This function scans an integer array to find the maximum value and returns the index of its first occurrence. I iterated through the input array, storing the maximum value in `t0` and its index in `t1`. In each iteration, I compared the current value with the maximum value. If the current value was larger, I updated both the maximum value and its index.
### mul
I wrote this function inline when needed. It is used to replace the `mul` instruction from the M extension. Suitable for environments that lack a multiplication instruction. First, I perform an AND operation between the multiplier and 1, if the result is 1, add the multiplicand to the current result. Then, right-shift the multiplier and left-shift the multiplicand. Repeat until the multiplier becomes 0.
### dot
This finction implement the dot product between two vectors. Due to the lack of multiplication instruction, I used my `mul` function to perform the multiplication operation.
### matmul
This function performs matrix multiplication by using the `dot` function that we implemented earlier to complete the operation. What I did was, after each iteration of the inner_loop, I moved the pointer `a0` to the next row of `M0` and incremented the loop counter `s0` by 1.
### read_matrix
This function reads a binary matrix from a file and load it into memory. The data will be stored in row-major order. Due to the lack of multiplication instruction, I used my `mul` function to perform the multiplication operation.
### write_matrix
This function writes a matrix to a binary file. The data will be written in row-major order. Due to the lack of multiplication instruction, I used my `mul` function to perform the multiplication operation.
### classify
This function brings everything together to classify an input using two weight matrices and the ReLU and ArgMax functions. Due to the lack of multiplication instruction, I used my `mul` function to perform the multiplication operation.

## Result








