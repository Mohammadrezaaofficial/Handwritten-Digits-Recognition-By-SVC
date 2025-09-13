# Handwritten-Digits-Recognition-By-SVC

This document appears to be a Jupyter Notebook or a similar file showing the steps to train a Support Vector Classifier (SVC) to recognize handwritten digits from the MNIST dataset. Here is a complete explanation of the process shown in the document.

## Summary
The document demonstrates how to use a Support Vector Classifier (SVC) to classify handwritten digits from the MNIST dataset. It shows the steps of loading the data, visualizing the images, preparing the data for the model, training the classifier, and then using the trained model to make predictions and evaluate its performance.

## 1. Data Loading and Visualization
The process begins with importing necessary libraries: pandas, numpy, and matplotlib.pyplot for data handling and visualization, and datasets from sklearn to access the MNIST digit dataset.

The MNIST dataset, consisting of 1797 images , is loaded. The document then shows how to display a single image from the dataset using matplotlib.pyplot. Each image is an 8x8 pixel grid , and the data.target attribute provides the corresponding digit label for each image. A list of images and their corresponding labels is created, and the first 10 digits are displayed in a subplot for a visual check.



## 2. Data Preparation
The sklearn.svm.SVC classifier expects a 2D array of data, where each row is a sample and each column is a feature. The original images are 8x8 matrices, and they need to be flattened into a single array of 64 values (8 * 8). The document shows how to reshape the images using data.images.reshape(len(data.images), -1) and stores it in the flatshape variable.

## 3. Model Training
A Support Vector Classifier (SVC) is imported from sklearn.svm. An instance of the SVC model is created with specific parameters, random_state=3432 and C=0.5. The model is then trained on the entire dataset using the svm_classifier.fit function with the flattened image data (flatshape) and their corresponding labels (y).

## 4. Prediction and Evaluation
The document demonstrates a prediction on a new, manually created image u. The image u is an 8x8 matrix that is then flattened and passed to the trained svm_classifier for prediction. The model successfully predicts that the digit is a '3'.To evaluate the model's performance on unseen data, a new SVC model (svm_new) is trained on a subset of the data (the first 1001 images and labels). It then predicts the labels for the remaining images (from index 1001 onwards). The predicted labels are then compared to the actual labels to evaluate the accuracy. The document also includes a confusion matrix to show the prediction results in detail.

## Conclusion
The document provides a clear, step-by-step example of using a Support Vector Classifier for handwritten digit recognition. It covers the complete machine learning workflow, including data preparation, model training, prediction on a new data point, and a final evaluation of the model's performance on a held-out test set. This showcases a practical application of a common machine learning algorithm.
