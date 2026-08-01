# Deep Learning Assignment 3

## Title

**Implementation of Forward Propagation and Backpropagation using TensorFlow/Keras on the Wine Dataset**

---

# Objective

The objective of this assignment is to implement a **Multi-Layer Perceptron (MLP)** using **TensorFlow/Keras** on the Wine Dataset and study the effect of different learning rates and the number of epochs on model performance.

---

# Dataset Description

The **Wine Dataset** is a well-known multi-class classification dataset available in the Scikit-Learn library.

It contains the chemical analysis of wines grown in the same region in Italy but derived from three different cultivars (wine classes).

The objective is to classify a wine sample into one of the three classes based on its chemical properties.

### Dataset Information

* Total Samples: **178**
* Number of Features: **13**
* Number of Classes: **3**

### Input Features

* Alcohol
* Malic Acid
* Ash
* Alcalinity of Ash
* Magnesium
* Total Phenols
* Flavanoids
* Nonflavanoid Phenols
* Proanthocyanins
* Color Intensity
* Hue
* OD280/OD315 of Diluted Wines
* Proline

### Target Classes

* Class 0
* Class 1
* Class 2

---

# Software and Libraries Used

* Python
* TensorFlow
* Keras
* NumPy
* Pandas
* Matplotlib
* Scikit-Learn

---

# Workflow

The assignment was completed using the following steps:

1. Import required libraries.
2. Load the Wine dataset.
3. Perform Exploratory Data Analysis (EDA).
4. Check dataset information and missing values.
5. Visualize class distribution.
6. Plot histograms of all features.
7. Analyze feature correlation.
8. Separate features and target.
9. Split the dataset into training and testing sets.
10. Standardize the features using StandardScaler.
11. Build a Multi-Layer Perceptron (MLP).
12. Compile the model.
13. Train the model.
14. Evaluate model performance.
15. Analyze the effect of different learning rates.
16. Analyze the effect of different numbers of epochs.
17. Draw conclusions.

---

# Data Preprocessing

Before training the neural network, the following preprocessing steps were performed:

* Separated input features (X) and target labels (y).
* Split the dataset into training (80%) and testing (20%) sets.
* Applied StandardScaler to standardize all input features.

Feature scaling ensures that all features have similar ranges, allowing the neural network to train more efficiently.

---

# Multi-Layer Perceptron (MLP)

A Multi-Layer Perceptron (MLP) is a feed-forward artificial neural network consisting of:

* Input Layer
* Hidden Layer(s)
* Output Layer

The architecture used in this assignment is:

* Input Layer: **13 neurons**
* Hidden Layer 1: **16 neurons (ReLU Activation)**
* Hidden Layer 2: **8 neurons (ReLU Activation)**
* Output Layer: **3 neurons (Softmax Activation)**

---

# Forward Propagation

Forward propagation is the process in which the input data moves through the neural network to generate predictions.

### Steps

1. Input features are provided to the input layer.
2. Each neuron calculates the weighted sum of its inputs.
3. The ReLU activation function is applied in the hidden layers.
4. Information flows through all hidden layers.
5. The Softmax activation function converts the outputs into probabilities.
6. The class with the highest probability is selected as the predicted output.

During this assignment, forward propagation was automatically executed by TensorFlow/Keras during:

```python
model.fit(...)
```

and

```python
model.predict(...)
```

---

# Backpropagation

Backpropagation is the learning algorithm used to improve the neural network after each prediction.

### Steps

1. Compare predicted output with actual output.
2. Calculate the loss using Sparse Categorical Crossentropy.
3. Compute gradients of the loss with respect to each weight.
4. Propagate the error backward through the network.
5. Update the weights using the Adam optimizer.
6. Repeat the process for every batch and every epoch.

In TensorFlow/Keras, backpropagation is automatically performed during:

```python
model.fit(...)
```

---

# Optimizer

The **Adam Optimizer** was used because it provides:

* Faster convergence
* Stable learning
* Adaptive learning rate
* Better optimization compared to traditional gradient descent

Learning Rate used for the base model:

```text
0.001
```

---

# Loss Function

The loss function used is:

```text
Sparse Categorical Crossentropy
```

This loss function is appropriate because the target labels are integer encoded (0, 1, and 2).

---

# Model Evaluation

The trained model was evaluated using:

* Test Accuracy
* Training Loss
* Validation Loss
* Precision
* Recall
* F1-Score
* Confusion Matrix
* Classification Report

These metrics were used to assess the overall performance of the MLP classifier.

---

# Learning Rate Analysis

Three different learning rates were tested:

* 0.1
* 0.01
* 0.001

### Observation

* A high learning rate can make training unstable and may overshoot the optimal solution.
* A very small learning rate results in slower learning.
* A learning rate of **0.001** provided stable convergence and good classification performance.

---

# Epoch Analysis

The model was trained using:

* 20 Epochs
* 50 Epochs
* 100 Epochs

### Observation

* Increasing the number of epochs improved the learning performance initially.
* Beyond a certain number of epochs, the improvement became smaller.
* Excessive epochs may eventually lead to overfitting.

---

# Results

The implemented Multi-Layer Perceptron successfully classified the Wine Dataset with high accuracy.

The evaluation metrics indicated that the model effectively learned the relationship between the input features and the target classes.

The learning rate and the number of epochs were found to significantly influence the training process and overall model performance.

---

# Conclusion

In this assignment, a Multi-Layer Perceptron (MLP) was successfully implemented using TensorFlow/Keras on the Wine Dataset.

Basic Exploratory Data Analysis (EDA) and data preprocessing were performed before model training. The input features were standardized using StandardScaler, and the dataset was divided into training and testing sets.

During model training, TensorFlow/Keras automatically performed forward propagation, loss calculation, backpropagation, and weight updates through the Adam optimizer.

The trained model was evaluated using accuracy, precision, recall, F1-score, confusion matrix, and classification report. The effects of different learning rates and different numbers of epochs were also analyzed.

Overall, the assignment demonstrated how neural networks learn from data using forward propagation and backpropagation and how hyperparameters such as learning rate and epochs affect the final model performance.
