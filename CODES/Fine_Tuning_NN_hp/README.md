# Fine-Tuning Neural Network Hyperparameters with Keras Tuner on Fashion MNIST Dataset

This repository contains the code and report for fine-tuning neural network hyperparameters using Keras Tuner on the Fashion MNIST dataset.

## Introduction

In this project, we aim to optimize neural network hyperparameters using Keras Tuner on the Fashion MNIST dataset. The dataset consists of 60,000 training images and 10,000 test images of fashion items categorized into 10 classes. The goal is to find the best hyperparameters that maximize the model's validation accuracy.

## Dataset Preparation

The Fashion MNIST dataset is loaded using TensorFlow's built-in dataset module. It is split into training and validation sets, with the validation set containing the last 5000 images from the training data.

## Hyperparameter Tuning

Three different hyperparameter tuning techniques have been implemented:

### Random Search Tuner

The `RandomSearch` tuner from Keras Tuner is utilized to search for optimal hyperparameters. It explores the hyperparameter space randomly and performs 5 trials to find the best model configuration.

### Hyperband Tuner

The `Hyperband` tuner is employed with the goal of maximizing validation accuracy. It utilizes the Hyperband algorithm for hyperparameter search and early stopping. The best model configuration is determined after 2 hyperband iterations.

### Bayesian Optimization Tuner

The `BayesianOptimization` tuner uses Bayesian optimization to efficiently explore the hyperparameter space. It performs 10 trials to find the best hyperparameters.

## Code Structure

The code is structured into different sections:

- Data Loading and Preparation
- Model Building Function with Keras Tuner
- Hyperparameter Search using Random Search, Hyperband, and Bayesian Optimization Tuners
- Callbacks for TensorBoard Visualization and Early Stopping

## Results and Conclusion

The results from the hyperparameter tuning process, including the best hyperparameters found and the corresponding validation accuracy for each tuner, are documented in the code. The most effective tuner among Random Search, Hyperband, and Bayesian Optimization can be identified based on the achieved validation accuracy.

For detailed code implementation, refer to the provided code snippets in the notebook.

Feel free to explore the provided code and experiment with different hyperparameter settings to optimize the neural network's performance on the Fashion MNIST dataset.

---

This README provides an overview of the project, the dataset used, the hyperparameter tuning techniques employed, and the code structure. It aims to guide users through the project and help them understand the process of fine-tuning neural network hyperparameters using Keras Tuner.

