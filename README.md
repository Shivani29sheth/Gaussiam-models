# Gaussian-models-from-scratch

In this project, we create and compare two Gaussian based models, namely Multivariate Gaussian models and Gaussian Mixture Models.

## Multivariate Gaussian models

Description:
A simple classifier using multivariate Gaussian models. Each class in the data is modeled by a single 3D Gaussian distribution.

Two different structures for the covariance matrices are considered for the model, which are:

- Each Gaussian uses a diagonal covariance matrix.
- Each Gaussian uses a full covariance matrix

Model Explanation:

We first start by loading and preprocessing the data. The data is loaded via the read csv method which render the data in a dataframe. Next, we convert the dataframe into numpy arrays and separate the labels from the input data. The input data is further normalized for faster processing and the binary labels are converted to 0, 1 labels for easier processing.
