# PCA_Assignment

## Project Overview

### Project Overview

This project was completed as part of Milestone Assignment 2 on Principal Component Analysis (PCA). The objective of the project is to analyze the Breast Cancer Wisconsin dataset from sklearn.datasets and reduce the dimensionality of the dataset using PCA.

As a Data Analyst at Anderson Cancer Center, the goal is to identify essential variables that can help simplify analysis while retaining the most important information within the dataset.

Additionally, Logistic Regression was implemented as a bonus task to evaluate how effectively the reduced dataset can be used for prediction.

### Objectives

The main objectives of this project are:

* Load and analyze the Breast Cancer dataset
* Standardize the dataset
* Apply Principal Component Analysis (PCA)
* Reduce the dataset into 2 principal components
* Visualize the transformed dataset
* Evaluate how much variance is retained after dimensionality reduction
* Implement Logistic Regression for prediction (Bonus Task)
* Technologies and Libraries Used

The following Python libraries were used:

* pandas
* numpy
* matplotlib
* scikit-learn

### Dataset Information

The dataset used is the Breast Cancer Wisconsin dataset available directly from Scikit-learn.

It contains:

* 569 samples
* 30 numerical features
* Target classes:
* Malignant
* Benign

The dataset includes features such as:

* Radius
* Texture
* Perimeter
* Area
* Smoothness
* Compactness


### Project Workflow

1. Import Libraries

Required Python libraries are imported for:

* Data handling
* Visualization
* Machine learning
* PCA implementation

2. Load the Dataset

The Breast Cancer dataset is loaded using:

from sklearn.datasets import load_breast_cancer

The features and target variables are separated into:

* X → Feature variables
* y → Target variable

3. Standardize the Dataset

Before applying PCA, the dataset is standardized using StandardScaler.

Why?

PCA is highly sensitive to differences in scale. Standardization ensures:

Mean = 0

Standard deviation = 1

This allows all variables to contribute equally.

Code used:

scaler = StandardScaler()

X_scaled = scaler.fit_transform(X)

4. Apply Principal Component Analysis (PCA)

PCA is implemented to reduce the original 30-dimensional dataset into 2 principal components.

Code used:

pca = PCA(n_components=2)

X_pca = pca.fit_transform(X_scaled)

The transformed dataset now contains:

Principal Component 1 (PC1)
Principal Component 2 (PC2)

These components retain most of the important information from the original dataset.

What is PCA?

Principal Component Analysis (PCA) is a dimensionality reduction technique used in machine learning and data analysis.

It works by:

* Identifying patterns in data
* Finding directions with maximum variance
* Transforming many variables into fewer components

Benefits of PCA:

* Reduces complexity
* Improves visualization
* Reduces computational cost
* Removes redundancy
* Explained Variance Ratio

The explained variance ratio shows how much information each principal component retains.

Code used:

print(pca.explained_variance_ratio_)

Example interpretation:

PC1 may retain approximately 44% of variance

PC2 may retain approximately 19%

Together, both components retain a significant portion of the dataset’s information.

Data Visualization

A scatter plot is created to visualize the dataset after dimensionality reduction.

The graph:

Displays the two PCA components
Separates malignant and benign cancer cases using colors

Visualization helps demonstrate how PCA simplifies complex data into two dimensions.

Logistic Regression (Bonus Task)

Logistic Regression was implemented to classify cancer cases using the two PCA components.

Steps performed:

* Split dataset into training and testing sets
* Train Logistic Regression model
* Predict test results
* Evaluate model performance

Code used:

model = LogisticRegression()
model.fit(X_train, y_train)
Model Evaluation

The following evaluation metrics were used:

Accuracy Score

Measures overall prediction accuracy.

Confusion Matrix

Shows:

* True Positives
* True Negatives
* False Positives
* False Negatives

Classification Report

Provides:

* Precision
* Recall
* F1-score

How to Run the Project in Jupyter Notebook

Step 1: Install Required Libraries

Run the following command:

pip install pandas numpy matplotlib scikit-learn

Expected Output

The notebook produces:

* Dataset preview
* PCA-transformed dataset
* Explained variance ratio
* PCA scatter plot
* Logistic Regression accuracy
* Confusion matrix
* Classification report

### Conclusion

This project successfully demonstrates the use of Principal Component Analysis (PCA) for dimensionality reduction on the Breast Cancer dataset.

The dataset was reduced from 30 features to 2 principal components while preserving significant information. Logistic Regression further demonstrated that the reduced dataset can still be effectively used for prediction and classification tasks.

The project highlights the importance of PCA in simplifying complex datasets and improving data visualization and analysis.
