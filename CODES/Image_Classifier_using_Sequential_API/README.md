# Fashion MNIST Classification with Keras

This repository contains code for implementing a simple convolutional neural network (CNN) to classify fashion articles based on the Fashion MNIST dataset. The CNN model is built using the Keras library in TensorFlow. This report describes the code, its functionalities, and provides insights into the results.

### Notebook Link : https://colab.research.google.com/drive/1B_OFguTF-CZDtO0ZhxzDBivXmEOKxag1?authuser=1#scrollTo=RNSkPVeLJjc2

# Code Overview:

## Data Loading:

The code loads the Fashion MNIST dataset using TensorFlow's built-in function.
It separates the data into training, validation, and testing sets.
Finally, it normalizes the pixel values to improve training performance.

## Model Definition:

The code defines a sequential Keras model.
It includes three hidden layers with 300 and 100 neurons each, respectively, using the ReLU activation function.
The output layer has 10 neurons representing the 10 clothing categories.
Softmax activation is used for the output layer to predict the probability distribution over the classes.
Model Training and Evaluation:

The model is compiled with the "sparse_categorical_crossentropy" loss function and the "sgd" optimizer.
It is trained for 30 epochs, with the validation set used to monitor overfitting.
After training, the model's performance is evaluated on the test set using both accuracy and loss metrics.
Visualizations and Predictions:

The code plots the training and validation accuracy curves to visualize the learning process.
It demonstrates the prediction process by predicting the class labels for three test images and showing their corresponding probabilities.
Detailed Report:

## 1. Data Preprocessing:

The script uses tf.keras.datasets.fashion_mnist.load_data() to conveniently load the Fashion MNIST dataset.
The x_train_full, y_train_full, and (x_test, y_test) variables store the training and testing data, respectively.
Further, the training data is split into training and validation sets using the last 5000 images for validation.
Finally, the pixel values of all images are divided by 255 for normalization, which is a common practice for image data in deep learning.

## 2. Model Architecture:

A sequential Keras model is defined using the tf.keras.Sequential() class.
The model consists of the following layers:
Input Layer: This layer accepts an input with the shape of each image (28 x 28).
Flatten Layer: This layer flattens the input into a 1D array of 784 features.
Dense Layers: Two hidden layers with 300 and 100 neurons, respectively, are added using the tf.keras.layers.Dense() function. These layers use the ReLU activation function for non-linearity.
Output Layer: A final Dense layer with 10 neurons and the Softmax activation function predicts the probability distribution over the 10 clothing categories.

## 3. Model Training and Evaluation:

The model is compiled with the following parameters:
Loss Function: "sparse_categorical_crossentropy" is used as the loss function, which measures the difference between the predicted and actual class probabilities.
Optimizer: "sgd" is used as the optimizer, which updates the model weights based on the calculated gradients.
Metrics: "accuracy" is used to track the model's performance in correctly classifying the images.

The model is trained for 30 epochs using the history = model.fit() method.
The x_train and y_train are used for training, and the x_valid and y_valid are used for validation.
After training, the model's performance on the test set is evaluated using the model.evaluate(x_test, y_test) method. This provides the final test accuracy and loss.

## 4. Visualizations and Predictions:

The training and validation accuracy curves are plotted using pandas and matplotlib to visualize the learning process.
Three test images are used to demonstrate the prediction capabilities.
The code predicts the class labels for these images using the model.predict(x_new) method.

Finally, it prints the predicted class names based on the index with the highest probability in the prediction matrix.
Further Analysis:

This model achieves a basic level of accuracy on the Fashion MNIST dataset.
The training and validation accuracy curves show that the model learns over time, but further optimization might be required for better performance.
Exploring different hyperparameters, such as the number of neurons, learning rate, or

## Contribution

Contributions are welcome! If you have a new use case to add or improvements to existing code, feel free to submit a pull request. Please follow the contribution guidelines outlined in the CONTRIBUTING.md file.

## Feedback

Your feedback is valuable. If you have suggestions, ideas, or encounter any issues, please open an issue or reach out through the contact information provided in the repository.

Let's dive into the exciting world of deep learning together! 🌟
