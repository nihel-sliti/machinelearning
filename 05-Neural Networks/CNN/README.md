# Convolutional Neural Network (CNN) for Binary Image Classification

This repository contains a Convolutional Neural Network (CNN) implemented in Python using Keras. The project classifies images as either "cat" or "not cat" using grayscale images.

## Features
- Converts images to grayscale and resizes them to 200x200 pixels.
- Builds a CNN with convolutional layers, pooling layers, and fully connected layers.
- Uses binary crossentropy for loss and Adam optimizer.
- Visualizes training and validation loss and accuracy.

## Dataset
- Images are stored in the folder `/content/drive/MyDrive/CNN/`.
- Images with names starting with `cat` are labeled as `1`, and others are labeled as `0`.
- The dataset is split into training (67%) and testing (33%) subsets.

## Model Architecture
1. **Input Layer**: Grayscale image of size 200x200x1.
2. **Convolutional Layers**:
   - 128 filters, 3x3 kernel, ReLU activation.
   - 64 filters, 3x3 kernel, ReLU activation.
3. **MaxPooling Layer**: Reduces dimensions with a 2x2 pool.
4. **Flatten Layer**: Converts 2D matrices to 1D vectors.
5. **Fully Connected Dense Layers**:
   - Dense layer with 512 units, ReLU activation.
   - Dense layer with 128 units, ReLU activation.
   - Final dense layer with 1 unit, sigmoid activation.

## Requirements
- Python 3.7+
- Libraries:
  - NumPy
  - OpenCV
  - Matplotlib
  - TensorFlow/Keras
  - scikit-learn

