# Assignment Number 2 : Iris Dataset 

## 📘 About the Dataset
The **Iris dataset** is a toy dataset in machine learning, 
It contains measurements of **150 iris flowers** across three species:
- Setosa
- Versicolor
- Virginica  

Each flower is described by four features:
- Sepal length (cm)
- Sepal width (cm)
- Petal length (cm)
- Petal width (cm)

The goal is to classify the species based on these features.

---

## 🔎 What We Have Done
1. **Data Loading & Inspection**  
   - Loaded the dataset using `sklearn.datasets.load_iris`.  
   - Converted it into a Pandas DataFrame.  
   - Viewed the first 10 rows and summary statistics.  

2. **Data Visualization (Matplotlib only)**  
   - Scatter plots to compare sepal and petal dimensions.  
   - Histograms to show feature distributions across species.  
   - Correlation heatmap to understand feature relationships.  

3. **Model Training**  
   - Split the dataset into training and testing sets (70/30).  
   - Trained a **Multi-Layer Perceptron (MLP)** classifier with two hidden layers.  

4. **Model Evaluation**  
   - Calculated accuracy score.  
   - Generated classification report (precision, recall, F1-score).  
   - Visualized confusion matrix.  

5. **Advanced Visualizations**  
   - Plotted the **loss curve** to show training convergence.    
---

## 🤖 Algorithm Used: Multi-Layer Perceptron (MLP)
The **MLPClassifier** is a feedforward neural network model.  
- It consists of input, hidden, and output layers.  
- Each neuron applies a weighted sum followed by a non-linear activation function.  
- The model is trained using **backpropagation** and gradient descent to minimize loss.  

In this assignment:
- Hidden layers: `(10, 10)` neurons.  
- Maximum iterations: `1000`.  
- Random state fixed for reproducibility.  

In our MLP model, we used the **ReLU (Rectified Linear Unit)** activation function for the hidden layers.  
- ReLU is defined as: \( f(x) = \max(0, x) \).  
- It introduces non-linearity, allowing the network to learn complex patterns.  
- Compared to sigmoid or tanh, ReLU is computationally efficient and helps avoid the **vanishing gradient problem**.  

By using ReLU, our MLP was able to converge faster and achieve high accuracy on the Iris dataset.

---

## ✅ Conclusion
This assignment demonstrates the **complete machine learning pipeline**:
- Data exploration  
- Visualization  
- Model training  
- Evaluation  

The Iris dataset remains a simple yet powerful example to understand classification tasks and neural network models.
