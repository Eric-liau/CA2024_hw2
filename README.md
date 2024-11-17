# Assignment 2: Classify

TODO: Add your own descriptions here.

## Functions
### abs
This function converts the input value to its absolute value. When the input value is negative, I use 0 minus the input value to implement the absolute value conversion.
### relu
This function converts every element x in input array to max(x,0).
### argmax
This function scans an integer array to find the maximum value and returns the index of its first occurrence. I iterated through the input array, storing the maximum value in `t0` and its index in `t1`. In each iteration, I compared the current value with the maximum value. If the current value was larger, I updated both the maximum value and its index.
### dot
This finction implement the dot product between two vectors. To replace the `mul` instruction, I perform an AND operation between the multiplier and 1, if the result is 1, add the multiplicand to the current result. Then, right-shift the multiplier and left-shift the multiplicand. Repeat until the multiplier becomes 0.
### matmul
This function performs matrix multiplication by using the `dot` function that we implemented earlier to complete the operation. What I did was, after each iteration of the inner_loop, I moved the pointer `a0` to the next row of `M0` and incremented the loop counter `s0` by 1.
### read_matrix







