# Fashion MNIST Assignment

### Project Overview

This project implements a Convolutional Neural Network (CNN) using TensorFlow/Keras in Python to classify images from the Fashion MNIST dataset. The objective of the project is to train a deep learning model capable of recognizing and classifying grayscale images of clothing items into their respective categories.

The project was completed as part of the Module 6 Assignment on image classification and deep learning. It demonstrates the practical application of CNNs in computer vision tasks, specifically image recognition and classification.

The Fashion MNIST dataset was used because it is a standard benchmark dataset for machine learning and deep learning experiments involving image classification.

### Objectives

The primary aim of this assignment was to:

* Develop a Convolutional Neural Network (CNN) with six layers using Keras
* Train the model on the Fashion MNIST dataset
* Evaluate the performance of the trained model
* Make predictions on at least two images from the dataset
* Understand the workflow of image classification using deep learning

This assignment also serves as an introduction to how AI systems classify images in real-world applications such as:

* facial recognition
* medical image analysis
* product recommendation systems
* autonomous vehicles
* retail and fashion technology

### Dataset Information

The Fashion MNIST dataset is a collection of grayscale images consisting of 10 categories of fashion items.

Each image:

* is 28 × 28 pixels
* is grayscale
* belongs to one of 10 clothing classes

The dataset contains:

* 60,000 training images
* 10,000 testing images

The classes include:

* T-shirt/top
* Trouser
* Pullover
* Dress
* Coat
* Sandal
* Shirt
* Sneaker
* Bag
* Ankle boot

### Project Workflow

The project followed the standard deep learning workflow for image classification:

* Importing required libraries
* Loading the Fashion MNIST dataset
* Preprocessing the dataset
* Building the CNN architecture
* Compiling the model
* Training the CNN
* Evaluating model performance
* Making predictions
* Visualizing prediction results

### Data Preprocessing

Before training the model, the dataset was preprocessed to improve performance and compatibility with the CNN architecture.

* Normalization : The image pixel values were normalized by dividing all values by 255.0. This converted pixel intensities from the range: 0-255 to 0-1. Normalization helps the neural network:

* train faster
* improve accuracy
* maintain stable learning

* Reshaping Images: The images were reshaped into the format:

(28, 28, 1)

This was necessary because CNNs require image data to include:

* height
* width
* color channels

Since Fashion MNIST images are grayscale, the channel value was set to 1.

### CNN Architecture

A Convolutional Neural Network (CNN) with six layers was developed using Keras Sequential API.

The architecture included:

* Convolutional Layer
* Max Pooling Layer
* Convolutional Layer
* Max Pooling Layer
* Flatten Layer
* Dense Layer

An output layer with Softmax activation was also included for classification into 10 categories.

### Explanation of CNN Components

* Convolutional Layers: The convolutional layers were responsible for detecting important image features such as:

* edges
* curves
* textures
* shapes

The first convolutional layer extracted simple patterns, while the second layer learned more complex clothing features.

* Max Pooling Layers: Pooling layers reduced the size of feature maps while preserving important information.

Their purpose was to:

* reduce computational complexity
* improve training efficiency
* prevent overfitting

* Flatten Layer: The flatten layer converted two-dimensional feature maps into a one-dimensional vector so the dense layers could process the information.

* Dense Layer: The dense layer combined the learned features to make classification decisions.

* Output Layer: The output layer used the Softmax activation function to generate probability scores for each clothing category.

The category with the highest probability became the model’s final prediction.

### Model Compilation

The model was compiled using:

* Adam optimizer
* Sparse categorical crossentropy loss function
* Accuracy evaluation metric

* Adam Optimizer: The Adam optimizer was used because it efficiently updates model weights during training and improves convergence speed.

* Loss Function: Sparse categorical crossentropy measured how far the model’s predictions were from the correct labels.

* Accuracy Metric: Accuracy was used to monitor how well the CNN classified images correctly.

### Model Training

The CNN was trained using the training dataset over multiple epochs.

During training, the model:

* made predictions
* calculated errors
* adjusted weights
* improved performance iteratively

Validation data was used during training to monitor the model’s generalization performance.

### Model Evaluation

After training, the model was evaluated using the testing dataset.

The evaluation process measured:

* test loss
* classification accuracy

This step determined how effectively the CNN could classify unseen images.

### Predictions

The trained model was used to make predictions on images from the testing dataset.

At least two images were selected and displayed alongside:

* predicted labels
* actual labels

This demonstrated the CNN’s ability to correctly identify clothing categories.

### Visualization

Matplotlib was used to:

* display Fashion MNIST images
* visualize predictions
* compare predicted and actual labels

Visualization helped confirm whether the model’s predictions were accurate.

### Conclusion

This project successfully demonstrated the implementation of a Convolutional Neural Network (CNN) for image classification using the Fashion MNIST dataset.

The CNN learned to identify patterns and features within clothing images and accurately classify them into their respective categories. The project provided practical experience with deep learning workflows and highlighted the effectiveness of CNNs in computer vision applications.

The knowledge gained from this assignment can be extended to more advanced AI applications involving:

* facial recognition
* object detection
* medical diagnostics
* retail recommendation systems
* autonomous systems
