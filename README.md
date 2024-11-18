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
```
test_abs_minus_one (__main__.TestAbs) ... ok
test_abs_one (__main__.TestAbs) ... ok
test_abs_zero (__main__.TestAbs) ... ok
test_argmax_invalid_n (__main__.TestArgmax) ... ok
test_argmax_length_1 (__main__.TestArgmax) ... ok
test_argmax_standard (__main__.TestArgmax) ... ok
test_chain_1 (__main__.TestChain) ... ok
test_classify_1_silent (__main__.TestClassify) ... ok
test_classify_2_print (__main__.TestClassify) ... ok
test_classify_3_print (__main__.TestClassify) ... ok
test_classify_fail_malloc (__main__.TestClassify) ... ok
test_classify_not_enough_args (__main__.TestClassify) ... ok
test_dot_length_1 (__main__.TestDot) ... ok
test_dot_length_error (__main__.TestDot) ... ok
test_dot_length_error2 (__main__.TestDot) ... ok
test_dot_standard (__main__.TestDot) ... ok
test_dot_stride (__main__.TestDot) ... ok
test_dot_stride_error1 (__main__.TestDot) ... ok
test_dot_stride_error2 (__main__.TestDot) ... ok
test_matmul_incorrect_check (__main__.TestMatmul) ... ok
test_matmul_length_1 (__main__.TestMatmul) ... ok
test_matmul_negative_dim_m0_x (__main__.TestMatmul) ... ok
test_matmul_negative_dim_m0_y (__main__.TestMatmul) ... ok
test_matmul_negative_dim_m1_x (__main__.TestMatmul) ... ok
test_matmul_negative_dim_m1_y (__main__.TestMatmul) ... ok
test_matmul_nonsquare_1 (__main__.TestMatmul) ... ok
test_matmul_nonsquare_2 (__main__.TestMatmul) ... ok
test_matmul_nonsquare_outer_dims (__main__.TestMatmul) ... ok
test_matmul_square (__main__.TestMatmul) ... ok
test_matmul_unmatched_dims (__main__.TestMatmul) ... ok
test_matmul_zero_dim_m0 (__main__.TestMatmul) ... ok
test_matmul_zero_dim_m1 (__main__.TestMatmul) ... ok
test_read_1 (__main__.TestReadMatrix) ... ok
test_read_2 (__main__.TestReadMatrix) ... ok
test_read_3 (__main__.TestReadMatrix) ... ok
test_read_fail_fclose (__main__.TestReadMatrix) ... ok
test_read_fail_fopen (__main__.TestReadMatrix) ... ok
test_read_fail_fread (__main__.TestReadMatrix) ... ok
test_read_fail_malloc (__main__.TestReadMatrix) ... ok
test_relu_invalid_n (__main__.TestRelu) ... ok
test_relu_length_1 (__main__.TestRelu) ... ok
test_relu_standard (__main__.TestRelu) ... ok
test_write_1 (__main__.TestWriteMatrix) ... ok
test_write_fail_fclose (__main__.TestWriteMatrix) ... ok
test_write_fail_fopen (__main__.TestWriteMatrix) ... ok
test_write_fail_fwrite (__main__.TestWriteMatrix) ... ok

----------------------------------------------------------------------
Ran 46 tests in 66.878s

OK
```








