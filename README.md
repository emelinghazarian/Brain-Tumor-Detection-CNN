# Brain Tumor Detection using CNN

## Overview
This project involves building, training, and evaluating Convolutional Neural Networks (CNNs) for the classification of MRI brain images into categories that indicate whether a brain tumor is present. The dataset used consists of grayscale MRI images, which are processed through several stages involving data preparation, model training, learning rate scheduling, and transfer learning to achieve high classification accuracy.

## Dataset
The dataset used for this project contains grayscale MRI images labeled as "Yes" (tumor) or "No" (no tumor). The dataset can be downloaded from the provided link:

[Download Dataset](https://drive.google.com/file/d/1sNlHFQKjyfcNE_smFT-7VT1oChmAUcPK/view?usp=sharing)

![image](https://github.com/user-attachments/assets/c18bcde1-8d3e-43e7-8bc4-fea70bd2b8c3)

After downloading, the dataset is split into:
- **Training set**: 70%
- **Validation set**: 15%
- **Test set**: 15%

## Project Steps

### Part 1: Data Preparation
1. **Download and Analyze the Dataset**:
   - Download the dataset and explore the images from both "Yes" and "No" classes.
   - Split the dataset into training, validation, and test sets in a 70-15-15 ratio.

### Part 2: CNN Model Training
1. **Build and Train the CNN Model**:
   - Design a CNN model using convolutional layers, Depthwise Separable Convolutions, Max Pooling, Fully Connected layers, and optional Residual Blocks.
   - Train the model for **30 epochs** using the training dataset.
   - Observe and plot **training and validation loss** and **accuracy** to evaluate the performance.
2. **Evaluate the Model**:
   - Evaluate the model on the test set using metrics like **Confusion Matrix**, **Overall Accuracy**, **Precision**, **Recall**, **F1-Score**, and **ROC Curve**.

### Part 3: Learning Rate Scheduling
1. **Implement Learning Rate Schedulers**:
   - Use **Cosine Annealing** and **ReduceLROnPlateau** strategies to dynamically adjust the learning rate during training.
   - Retrain the model for **30 epochs** and compare the results with the original training to observe the effect of these schedulers on learning.

### Part 4: Regularization Techniques
1. **Early Stopping**:
   - Implement **Early Stopping** to halt training when validation loss stops improving for 3 epochs.
2. **L2 Regularization**:
   - Add **L2 Regularization** to the loss function and retrain the model for **30 epochs**.
3. **Dropout**:
   - Add **Dropout** layers to the model and train for **30 epochs** to prevent overfitting.

### Part 5: Transfer Learning
1. **Use Pre-trained Models**:
   - Use pre-trained models like **ResNet-18** to classify MRI images by adding new classification layers on top.
2. **Fine-tune the Models**:
   - Freeze the initial layers, add new layers, and train the model on MRI images for **30 epochs**.
   - Unfreeze all layers and fine-tune the entire model, observing the impact on accuracy.


## Results
- The results of the training, including **accuracy**, **precision**, **recall**, **F1-Score**, and **Confusion Matrix** are saved in the `results/` directory.
- Graphs of **training/validation accuracy** and **loss** are plotted to observe model performance and overfitting.



