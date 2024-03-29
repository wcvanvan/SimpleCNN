# Simple CNN in C++
The forward propagation part of a CNN written in C++。

It's capable of distinguishing human and landscape photos using the model trained by the library "<a href="https://github.com/ShiqiYu/SimpleCNNbyCPP">SimpleCNNbyCPP</a>" (written by my teacher).

This simple CNN model contains 3 convolutional layers, 2 max-pooling layers and 1 fully-connected layer.

## Features
The core of this project is a self-made matrix class, high speed matrix multiplication and convolution

+ matrix class possesses soft-copy function, performant in the scene of image copying

+ matrix multiplication utilized various skills to obtain high speed, including partitioning matrices into smaller blocks and SIMD (crossed-platfrom achieved)

+ im2col algorithm is implemented to turn convolution operation into matrix multiplication. After im2col, we only need to do multiplying a 1 x K matrix with a K x N matrix, which I specifically do optimization. Finally this kind of multiplication reaches the same speed with OpenBLAS (one of the fastest libraries)

## How to use
Check out main.cpp, and change the image path

The program will provide two numbers after running, one indicates the possibility that the picture is a human face, the other indicates the possibility of scenery.





