# Optimizing-the-test-time-for-Mercedez-Benz-for-Greener-Manufacturing

## Keywords: Deep Learning, Neural Networks, PCA, Feature Engineering.

### Problem statement:
Mercedes-Benz is the leader in the premium car industry. With a huge selection of features and options, customers can choose the customized Mercedes-Benz of their dreams.To ensure the safety and reliability of every unique Mercedez Benz configuration before they hit the road, the company’s engineers have developed a robust testing system. As one of the world’s biggest manufacturers of premium cars, safety and efficiency are paramount on Mercedes-Benz’s production lines. However, optimizing the speed of their testing system for many possible feature combinations is complex and time-consuming without a powerful algorithmic approach. Thus, we need to reduce the time spnt by the car. Optimal algorithm will contribute to faster testing, resulting in lower carbon dioxide emissions without reducing Mercedes-Benz’s standards.

### Datset:
[Dataset Link](https://www.kaggle.com/c/mercedes-benz-greener-manufacturing/data)

This is a regression type Machine Learning problem. We are given a dataset with 572 independent features and 1 dependent target variable. Target variable is the time spent by the car on test-bench.

### Approach:

1. Feature Engineering:

We did Exploratory Data Analysis on the features and cleaned the dataset by removing the NULL values as the constituted to less than 1% of the dataset. 
Categorical features were one hot encoded after binning the low-frequency in one separate category. Some binary features were dropped which had only one value for all the data points.
Applied Principal Component analysis on Dataset to reduced the dimensions retaining 80% variance. The number of dimensions after PCA were 45.

2. Deep Learning Implementation:

Developed Artificial Neural Network in tensorflow-keras library. There were 2 hidden layers in the NN. Activation function used in all the layers is ReLu. Compiled the Model using 'adam' optimiser and 'mse' loss  The dataset was split into k=5 folds for k-fold cross validation. The model was trained with 100 epochs and batch size 32. 

For Code & detailed approach, please refer the [Notebook](https://github.com/hrushikesh-shelar/Optimizing-the-test-time-for-Mercedez-Benz-for-Greener-Manufacturing/blob/main/Greener_Manufacturing_Mercedes_Benz_Project.ipynb)

### Results:
The metric for result was R2 Score. The training R2 score was 0.61 and test R2 score was 0.475
