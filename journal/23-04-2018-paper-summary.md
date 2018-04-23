# April 23, 2018

Summary of the paper ``Star-galaxy Classification Using Deep Convolutional Neural Networks``.

# Summary of ``Star-galaxy Classification Using Deep Convolutional Neural Networks``
- deep convolutional neural networks allow a machine to automatically learn the features directly from data, minimizing the need for input from human experts
- there have been other successful attempts at similar problems using decision trees, support vector machines, and classifier combination strategies
- cross-validation is often avoided in deep learning in favor of hold-out validation, since cross-validation is computationally expensive
- activation function used is leaky ReLU (for faster training and to avoid dead neurons)
- loss function used is cross-entropy
- used mini-batch gradient descend to compute the bias and weight updates
  - there's a trade-off: the lower the batch size, the lower the convergence rate will be; the larger the batch size, the longer it will take to compute the gradient at each step
  - a moderate batch size with a decaying learning rate is generally used in practice
  - a batch size of ``128`` was used for the experiments
- the input to a convolutional layer is an image, and the output channels of each layers are called feature maps
- to produce output feature maps, each feature map is convolved with a set of weights called filters (and apply a non-linearity such as ReLU)
- typically a pooling layer computes the maximum of a local ``2x2`` patch in a feature map (this results in dimensionality reduction)
- learning rate was initialized to ``0.003`` for all layers and linearly decreased from ``0.003`` to ``0.0001`` over ``750`` epochs
- biases had values of ``b=0.01`` or ``0.1``
- data augmentation techniques (label-preserving transformations)
  - rotation: randomly rotate images by a multiple of 90 degrees
  - reflection: flip images horizontally with a probability of ``0.5`` to exploit mirror symmetry
  - translation: ???
  - Gaussian noise: introduce random Gaussian noise to each pixel value
- implemented dropout to force neurons to learn more robust features
- when evaluating the performance, using a fixed threshold ignores the model's operating conditions
  - need to research other methods for how to evaluate a probabilistic model (MSE, AUC, ROC, completenesses and purity, etc)
