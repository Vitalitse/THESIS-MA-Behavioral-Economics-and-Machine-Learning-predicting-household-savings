# THESIS-MA-Behavioral-Economics-and-Machine-Learning-predicting-household-savings
Our main purpose in this thesis is to build a model that will predict saving behavior of households using demographics, psychological characteristics, and situational factors based on theoretical and empirical findings. In some cases, research in psychology measures the accuracy of a model based on the fitness between the model and the sample data, or whether the size or direction of a coefficient matches the theoretical explanation, but lacks the accuracy when it comes to predicting behavior. Using machine learning techniques that are testing out of sample data, we will be able to increase the understanding of the existing theories and findings (Yarkoni &amp; Westfall, 2017).

Out target variable is a class which include amount of savings.
We run our models with all 7 classes, and also with 3 classes - Low, Mid and High.

As the data is highly imbalanced - one vs all, we are using F1 weighted score and Recall Precision curve.

## Process:
- Data preprocessing: the data is a survey data, categorical values already encoded.
- Change columns names into meaningful names.
- Remove columns with target leakedge.
- Remove columns with high correlation.
- Replace unanswered questions with NA and complete missing values. Large % of missing values, we will investigate and replace manualy, low % of missing values using KNNImputer and MICE.

## Model:
 - Split the data into train and test and use cross validation.
 - Use pipeline with OverSampling and StandartScaler.
 - Tune hyperparameters.
 - Models: Logistic regression, SVC, Decision Tree, Random Forest, XGBoost, LightGBM, KNN and Neural Networks.
 - Try improve results using clustering, Kmodes as the data is categorical.

## Conclusion
- We are investigating the results and drawing insights using SHAP for each class.
- The best scores so far: 7 classes, F1 weighted score of 39% with Neural Networks, and for 3 classes 70%
