# customer_segmentation

### I Introduction & Motivation:

Hello all,
in this repository is the code for my final project of the Data Science Nanodegree's from Udacity. The task was to cluster demographic data and compare it with customer data. In addition, predictions were to be made as to whether people are suitable as customers or not. There were several projects available (e.g. Image Recognition to identify dog breeds), but I chose this project because it had the most practical relevance for me. In addition, the unsupervised learning part appealed to me, since I had no experience in this area before.

### II Methodology:

The project is roughly divided into 3 parts: data cleaning, unsupervised leanring and supervised learning.

During the data cleaning part I analyze the provided data (unfortunately I am not allowed to share it) and do feature engineering accordingly. That means I impute nan values and drop certain features based on different criteria.

In the unsupervised part, I scale the features and apply PCA to reduce the dimensionality of the features. Then I use KMeans to cluster the data. I first cluster data representing the general universe. Then I take customer data and contrast the cluster distribution of the data sets to define over- or under-represented clusters.

In the supervised part, I use a similar data set to predict whether a person can be acquired as a customer. I test different algorithms (RandomForest, AdaBoost and XGBoost). Based on the best algorithm, I do hyperparameter tuning to optimize the model. The score used is ROC AUC, which is particularly well suited for binary classification problems.

To see in detail what I did, please check the Jupyter Notebook or my Medium post on this topic:
https://tobias-praetori91.medium.com/customer-segmentation-using-machine-learning-1593f107e6d6

## III Libaries:

The following libraries were used during the project:

- `numpy`
- `pandas`
- `time`
- `matplotlib`
- `seaborn`
- `textwrap`
- `imblearn`
- `sklearn`
- `xgboost`
- `pickle`

Google colab specific:
- `pydrive.auth`
- `google.colab`
- `oauth2client.client`

### IV Files:

| Name                          | Description                                        |
| ----------------------------- |----------------------------------------------------|
| CustomerSegmentation.ipynb    | Contains all the code I used for all three parts   |
| LICENSE                       | MIT License                                        |
| README.md                     | This README file                                   |
| meta_data.xlsx                | Contains meta data about the data sets             |

### V Results:

During the unsupervised part, I identified 13 clusters, 3 of which were disproportionately represented in the customer data. All clusters had in common that they contained mostly elderly and affluent individuals.

For the supervised part, I tested several algorithms, but XGBoost turned out to be superior. Through hyperparameter tuning, I tested different configurations. The final model was able to achieve a ROC AUC score of 0.80415, which earned me a place in the top 15 percent in the Kaggle competition.

I think there are several approaches to how the ROC AUC score could be further improved. Among others, I believe that further feature engineering could lead to significant improvements. With additional hyperparameter tuning, one could probably achieve some (smaller) improvements. If in the future an algorithm is established that is even better than XGBoost, it would probably be possible to achieve even better scores.

### VI Sources:

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

### VII Acknoledgments:

I would like to thank Udacity, Kaggle and Arvato for providing this great data set.
