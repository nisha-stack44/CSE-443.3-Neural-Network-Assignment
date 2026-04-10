***** Problem Set 02: Bank Term Deposit Prediction using Logistic Regression

** Objective
The objective of this project is to build a machine learning model that can predict whether a bank customer will subscribe to a term deposit based on their demographic and financial information.

** Dataset
The dataset used in this project is the Bank Marketing Dataset. It contains 17 different attributes such as age, job, marital status, 
balance, loan status, and previous marketing campaign information. The target variable is 'y', which indicates whether the customer subscribed to a term deposit (yes or no).
The dataset was loaded from the Kaggle environment, where it was processed using Python (pandas).

***** Methodology
Data Preprocessing: Initially, the dataset was loaded using pandas. Since several columns contained categorical values (such as job, marital status, etc.), 
those columns were converted into numerical values using Label Encoding. This step was necessary because machine learning models require numerical input.
 After that, the dataset was divided into input features (X) and the target variable (y).

Train-Test Split : The dataset was split into training and testing sets using an 80:20 ratio. The training data was used to train the model, while the testing data was used to evaluate its performance.

Feature Scaling : To improve model performance, feature scaling was applied using StandardScaler. This ensures that all features are on a similar scale and prevents any single feature from dominating the model.

Model Building : A Logistic Regression model was used for this binary classification problem. This model is simple, efficient, and suitable for predicting two possible outcomes.

*****Evaluation Metrics
The model was evaluated using:
- Accuracy
- Confusion Matrix
- Precision, Recall, and F1-score

*****Results
The model achieved an accuracy of approximately **88.78%** on the test dataset.

*****Confusion Matrix:
From the classification report:
- Precision for class 0: 0.90
- Recall for class 0: 0.98
- Precision for class 1: 0.60
- Recall for class 1: 0.22

*****Findings
The model performs very well in predicting customers who will not subscribe to a term deposit (class 0). However, it struggles to correctly identify customers who will subscribe (class 1). 
This happens because the dataset is imbalanced, where the number of "no" cases is much higher than "yes" cases. As a result, the model is biased toward the majority class.
