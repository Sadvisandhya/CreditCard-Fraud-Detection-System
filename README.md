# My_projects
Credit card fraud detection
Problem statement
The myriads of plastic cards in use worldwide are a gold mine for criminals. By 2027, financial service providers are expected to take a $40 billion hit globally in credit card losses, a significant increase compared to $27.85 bn in 2018.
The coronavirus pandemic is also fueling explosive growth in card fraud activity.
With global credit card fraud loss on the rise, it is important for banks, as well as 
e-commerce companies, to be able to detect fraudulent transactions. 

Data
●	The dataset is taken from Kaggle contains transactions made by credit cards in September 2013 by European cardholders.
●	This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.
●	It contains only numerical input variables which are the result of a PCA transformation. Features V1, V2, … V28 are the principal components obtained with PCA

●	The only features which have not been transformed with PCA are 'Time' and 'Amount'. 
●	Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction Amount, this feature can be used for example-dependant cost-senstive learning. 
●	Feature 'Class' is the target variable and it takes value 1 in case of fraud and 0 otherwise. 
●	It is a Binary classification Task

Data Pre-processing and Modelling
       
●	Fraud detection is a binary classification task in which any transaction will be predicted and labelled as a fraud or legit. This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.
●	Splitting the data into train and test set with 70% for training the model and 30% for evaluation
●	Creating a training data set that will allow our algorithms to pick up the specific characteristics that make a transaction more or less likely to be fraudulent. Using the original data set would not prove to be a good idea for a very simple reason: Since over 99% of our transactions are non-fraudulent, an algorithm that always predicts that the transaction is non-fraudulent would achieve an accuracy higher than 99%. Nevertheless, that is the opposite of what we want. We do not want a 99% accuracy that is achieved by never labeling a transaction as fraudulent, we want to detect fraudulent transactions and label them as such.
●	Dealing with Imbalanced Data using Oversampling and Under sampling techniques
●	Under sampling techniques used 
Random Under Sampler
●	Over sampling techniques used
SMOTE, ADASYN


●	Following models were tried using the oversampled and under sampled data
Logistic Regression
      Decision Trees
      Random Forest Classifier
      XGB Classifier
      Stacking
●	Along with the above supervised classification models also tried Clustering with tSNE and Auto encoders with Neural Network

Evaluation

•	F1 score as metrics as F1 Score is Harmonic Mean of Precision and Recall, it solves the problem of Precision-Recall Trade off. The higher the AUC (Area Under Curve) of the PR Curve, the better the model is in maximizing the trade-off between precision and recall (higher recall and precision in total compare to lower PR-AUC model). Average Precision is equal to the AUC of PR Curve.
•	Random forest with smote, hyper tuning gave the best result having 86%, 88%, 87
recall, precision and F1score respectively
