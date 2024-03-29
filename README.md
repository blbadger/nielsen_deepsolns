# Nielsen-deep-learning-solutions

Program for a neural network in Nielsen's excellent book (http://neuralnetworksanddeeplearning.com) with solutions to problems in Chapter 3, as noted.  Modified from the network2 code written by Nielsen and rewritten python3 by Dobrzanski (https://github.com/MichalDanielDobrzanski/DeepLearningPython35).

General notes: network2_with_ch3_problem_solutions.py contains most modifications: early stopping, learning rate decay, L1 or L2 regularization, and an option for momentum-based gradient descent. 

network2-parallel.py also implements an early stopping and learning rate decay options but most importantly parallelizes backpropegation across all minibatch elements using only numpy arrays.  For MNIST digit training, this yields a ~2x speed increase for a minibatch size of 20 and a 4x increase of the same for a minibatch of 100, a relatively modest result partly because numpy does not multithread by default.
