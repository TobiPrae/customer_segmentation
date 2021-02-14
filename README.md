# customer_segmentation

### I Introduction & Methodology:

Hello all,

in this repository is the code for my final project of the Data Science Nanodegree's from Udacity. The project is roughly divided into 3 parts: Data Cleaning, Unsupervised Leanring and Supervised Learning.

During the data cleaning part I analyze the provided data (unfortunately I am not allowed to share it) and do feature engineering accordingly. That means I impute nan values and drop certain features based on different criteria.

In the Unsupervised Part, I scale the features and apply PCA to reduce the dimensionality of the features. Then I use KMeans to cluster the data. I first cluster data representing the general universe. Then I take customer data and contrast the cluster distribution of the data sets to define over- or under-represented clusters.

In the supervised part, I use a similar data set to predict whether a person can be acquired as a customer. I test different algorithms (RandomForest, AdaBoost and XGBoost). Based on the best algorithm, I do hyperparameter tuning to optimize the model. The score used is ROC AUC, which is particularly well suited for binary classification problems.

To see in detail what I did, please check the Jupyter Notebook or my Medium post on this topic:
https://tobias-praetori91.medium.com/customer-segmentation-using-machine-learning-1593f107e6d6

### II Results:

...

### III Sources:

##### Part 1: Customer Segmentation Report
- https://towardsdatascience.com/unsupervised-learning-and-data-clustering-eeecb78b422a
- https://towardsdatascience.com/pca-using-python-scikit-learn-e653f8989e60
- https://colab.research.google.com/github/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/05.09-Principal-Component-Analysis.ipynb
- https://medium.com/@dmitriy.kavyazin/principal-component-analysis-and-k-means-clustering-to-visualize-a-high-dimensional-dataset-577b2a7a5fe2
- https://towardsdatascience.com/10-tips-for-choosing-the-optimal-number-of-clusters-277e93d72d92

##### Part 2: Supervised Learning Problem
- https://neptune.ai/blog/f1-score-accuracy-roc-auc-pr-auc
- https://machinelearningmastery.com/xgboost-for-imbalanced-classification/
- https://machinelearningmastery.com/smote-oversampling-for-imbalanced-classification/
- https://www.analyticsvidhya.com/blog/2017/03/imbalanced-data-classification/

### IV Acknoledgments:

I would like to thank Udacity, Kaggle and Arvato for providing this great data set.
