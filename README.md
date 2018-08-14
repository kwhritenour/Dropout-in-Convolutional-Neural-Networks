# Dropout-in-Convolutional-Neural-Networks

Dropout is found to be ineffective when used in conjunction with convolutional layers despite the fact that Convolutional neural networks (CNNs), while powerful with large datasets, are very prone to overfitting when trained on smaller datasets. This work aims to implement a modified version of the Dropout layer with continuous relaxation of dropout weights with increase in depth of the network and variant dropout weights for different neurons to be implemented after each Convolutional layer in order to stay overfitting in CNNs.
This modified layer will have probability of dropping a neuron proportional to the depth of the network and varying dropout weights across neurons, giving each neuron a unique probability of being dropped. This will achieve the goal of both regularizing the output of the convolutional layer in place of batchnorm and sparsifying the parameters of each layer making it less likely to overfit and quicker at training.

Significant work has been done to improve Dropout, including: 
* [Concrete Dropout, where the dropout weight hyper parameter is automatically tuned.](https://arxiv.org/pdf/1705.07832.pdf)
* [Gaussian Dropout, where dropout probabilities are sampled from a Gaussian Distribution and introduced as multiplicative Gaussian noise instead of binary dropping of weights.](http://mlg.eng.cam.ac.uk/yarin/PDFs/Dropout_as_a_Bayesian_approximation.pdf)
* [Variational Dropout, where Gaussian Dropout can be viewed as a form of Bayesian Regularization, thus allowing "individual dropout weights for each weight, neuron, or layer".](http://proceedings.mlr.press/v70/molchanov17a/molchanov17a.pdf)

These three main results will be used in the derivation of this project's modified Dropout Layer.
