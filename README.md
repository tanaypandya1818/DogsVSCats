# README: Cat-Dog Image Classification using Convolutional Neural Network (CNN)

## Overview:

This code implements a Convolutional Neural Network (CNN) for classifying images as either cats or dogs. The dataset used is from the Kaggle "Dogs vs. Cats" competition, where the task is to distinguish between images of cats and dogs.

## Directory Structure:

- **TRAIN_DIR:** Directory containing training images.
- **TEST_DIR:** Directory containing test images.
- **ROWS, COLS, CHANNELS:** Dimensions of the images (64x64 pixels with 3 color channels).
- **modelx:** CNN model built using Keras.

## Data Preparation:

1. The script reads and preprocesses the training and test images.
2. Training images are labeled as 1 for dogs and 0 for cats.
3. The data is shuffled and split into training and validation sets.

## Model Architecture:

The CNN model (`modelx`) consists of the following layers:

1. Convolutional layer with 32 filters and ReLU activation.
2. Max pooling layer.
3. Convolutional layer with 64 filters and ReLU activation.
4. Max pooling layer with dropout.
5. Convolutional layer with 128 filters and ReLU activation.
6. Max pooling layer with dropout.
7. Convolutional layer with 256 filters and ReLU activation.
8. Max pooling layer with dropout.
9. Convolutional layer with 512 filters and ReLU activation.
10. Flatten layer with dropout.
11. Fully connected layer with 120 units and ReLU activation.
12. Output layer with 2 units and sigmoid activation.

## Model Training:

The model is trained using the Adam optimizer and categorical cross-entropy loss. The training is carried out for 50 epochs with a batch size of 64.

## Results:

The model achieves a validation accuracy of around 89.46% after 50 epochs.

## Model Evaluation:

The script includes a function (`show_image_prediction`) to visualize predictions on random test images.

## How to Use:

1. Ensure that you have the required libraries installed (OpenCV, NumPy, Pandas, Matplotlib, TensorFlow, and Scikit-Learn).
2. Update the `TRAIN_DIR` and `TEST_DIR` variables with the correct paths to your training and test image directories.
3. Run the script to train the model.
4. Use the `show_image_prediction` function to visualize predictions on test images.

Note: This code assumes that the dataset follows a specific naming convention (contains "cat" or "dog" in the file name) and may need modification for different datasets.
