# Convolutional Neural Network

CNN are powerful architecture generally used for image analysis. The are highly efficient and perform better than the vanille version Multilayer Perceptron.
They are fast as the number of parameters required for training is drastically low than number of parameters in a MLP.

My task of this assignment was to try different CNN architectures and analyze the effect of different hyperparameters like Padding, Striding, etc.

The results are as follows

Model | Conv Layer | No. of Filters | Filter Size| MLP| Pooling_size | Padding | Strides |Training Acc | Testing Acc
--- | --- | --- | --- | --- | --- | --- | --- | --- | --- 
1 | 3 | 16-32-64 | 3-3-3 | 64-10 | (2x2)x2 | VALID | None | 0.69 | 0.66
2 | 4 | 8-16-32-64 | 2-3-4-5 | 64-10 |(2x2)x1 | VALID | None | 0.71 | 0.68
3 | 3 | 64-128-256 | 3-3-3 | 128-64-32-10 | (2x2)x2 | VALID | None | 0.82 | 0.73
4 | 4 | 128-256-512 | 2-2-2 |128-64-32-10 | (2x2)x2 | VALID | None | 0.96 | 0.72
5 | 6 | 8-16-32-64-128-256 | 5-5-5-5-5-5 | 64-10 | None | VALID | None | 0.73 | 0.63
6 | 3 | 64-128-256 | 3-3-3 | 64-10 | (2x2)x2 | SAME | None | 0.97 | 0.75
7 | 4 | 64-128-256-256 | 3-3-3-3 | 64-10 | (2x2)x3 | SAME | None | 1.0 | 0.75
8 | 4 | 64-128-256-256 | 3-3-3-3 | 64-10 | (2x2)x3 | SAME | 2 | 0.97 | 0.71
9 | 2 | 64-128 | 3-3 | 64-10 | 2x2 | VALID | 2 | 0.78 | 0.69
10 | 1 | 512 | 32 | 64-10 | None | VALID | None | 0.52 | 0.47
11 | 1 | 32 | 1 | 64-10 | None | VALID | None | 0.5 | 0.48
12 | 6 | 32-32-64-64-256-256 | 3-3-3-3-3-3 | 128-10 | (2x2)x3 | SAME | None | 0.96 | 0.77
