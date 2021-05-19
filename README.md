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

Now, to build a binary classifier using multivariate Gaussian models, we build a class called GDA that consists of all model functions and parameters. We initialize the model with the training data and separate the two classes to model their individual Gaussian distributions.

Next, for each class we compute the mean and covariance matrix for the Gaussian distribution and the diagonal elements of the full covariance matrix are taken to build the diagonal covariance matrix for each class. We thus complete the training part of the model and print the mean vectors, covariance vectors, and diagonal vectors for both classes. Next, we evaluate the model on the test data. The predict function takes in the test data and the co var mat parameter which takes the full covariance matrix for prediction if set to 0, else takes the diagonal covariance matrix. Thus, for every point in the test data, its probability is computed for both the classes, and the point is assigned to the class with a higher probability. This probability is computed using the MAP decision rule. We call the predict function for both the full covariance matrix and the diagonal covariance matrix, and compare the accuracy between the two. We thus obtain the following results for the experiment: 

(add image)

From the results, we observe that the multivariate Gaussian model does not fit the training data very well due to its high dimension and thus requires a more complex model. This can be verified with the accuracies obtained on the test data where the model performs slightly better with the diagonal covariance matrix.


## Gaussian Mixture Models

Description:
To improve the Gaussian classifier from the multivariate Gaussian model by using a Gaussian Mixture Model to model each class.

Investigate the Gaussian Mixture Models that have 2, 4, 8, or 16 Gaussian components and determine the best model configuration in terms of the number of Gaussian components and the covariance matrix structure (diagonal vs. full) for the given data set.
