# April 23, 2018

Report outline based on the paper ``Star-galaxy Classification Using Deep Convolutional Neural Networks`` ([see summary](./23-04-2018-paper-summary.md))

# Report Outline (rough draft)

## Title

## Abstract

## Introduction
- what problem are we trying to solve?
- motivate why is it interesting
- state contributions

## Body
- data
  - explain how data was chosen (cannot use the entire dataset, too large)
  - discuss data attributes (features, labels, etc)
  - is there any class imbalance?
  - data split (training, validation, and test)
- deep learning introduction
  - what are neural networks? (input -> weight and bias -> activation -> output)
  - activation function
  - loss function
  - how to update weights and bias?
  - learning rate
  - mini-batch gradient descent
- convolutional neural networks
  - define convolutional and pooling layers
  - how does dimensionality reduction happen?
- network architecture
  - this is well explained in table 1 in the paper
  - what values were used for batch size, learning rate, biases?
  - how were the weights initialized?
- regularization
  - a CNN has many weights, and there are many training samples (high change of overfitting)
  - data augmentation: usage of label-preserving transformations
  - dropout: forces neurons to learn more robust features
- results and discussion
  - show different ways to evaluate the performance of a classifier
  - discuss what are the best ways to evaluate a probabilistic classifier

## Related work

## Conclusions and future work
- summarize contributions
- acknowledge weaknesses

## References
