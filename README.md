In this project, the k-Nearest Neighbors (kNN) algorithm is applied to the famous Iris dataset to solve a classification problem. The Iris dataset consists of 150 observations from three different species of Iris flowers (Iris setosa, Iris virginica, and Iris versicolor), with 4 features: sepal length, sepal width, petal length, and petal width.

Objectives:
Data Loading and Inspection:

The data is loaded into a pandas DataFrame, and the columns are named according to the data description.

The dataset is examined by displaying the first 5 rows and creating scatter plots to visualize relationships between features (sepal width vs. sepal length, petal width vs. petal length) for each Iris species.

Data Preparation:

The feature variables (X) and response variable (Y) are prepared using pandas operators. Data is then split into training and test sets using train_test_split from scikit-learn.

Model Training and Prediction:

The kNN classifier is instantiated and trained using the training data.

Predictions are made on the test data, and the accuracy of the predictions is computed by comparing them with the true values (Y from test set).

The number of correct and incorrect predictions is also counted.

Model Evaluation with Varying k:

The impact of different values of k (number of neighbors) on the classifier’s performance is evaluated. A range of k values (1, 3, 5, 7, 10, 20, 30, 40, and 50) is tested.

For each value of k, 10 random train/test splits are generated. The model is fitted, predictions are made, and accuracy scores are averaged.

A plot is created to visualize how the accuracy score changes with varying k values.

Findings:
Best Performance: The kNN classifier performs best with smaller k values, particularly k = 3 and k = 5, achieving accuracy scores above 97%. This suggests that the model is effectively capturing local patterns in the data.

Underfitting with Larger k: As the number of neighbors increases (beyond k = 5), the model starts to underfit the data, leading to a decline in accuracy. This is particularly noticeable when k = 50, where the accuracy drops to approximately 89.7%.

Conclusion:
Smaller values of k are more suitable for the Iris dataset as they preserve the model's ability to differentiate between the Iris species accurately. The findings highlight the importance of choosing the right value for k to balance model complexity and accuracy.
