# FraudDetection

## 1. Data cleaning including missing values, outliers and multi-collinearity.
Dataset, although there were many transactions which had Old Original Balance that was zero but transaction happened. More than 1/4 of the dataset had the balances equal to Zero. Although most of them were categorized as Fraud. Also, one thing to be noted is that it will be better to mention the local currency or follow a constant currency because that can help in analyzing the data more efficiently.
Post and Pre Balances of the bank account were highly correlated with each other. We removed these features and inplace added the amount transferred and the amount added to the DataFrame.

## 2. Describe your fraud detection model in elaboration.
The Random Forest Algorithm is the foundation of my fraud detection model because the dataset has a huge imbalance of Non-Fraudulent Customers to that of Fraudulent Customers. Random Forest is the best ensemble learning technique for an imbalanced dataset since it combines different decision trees to produce a final prediction. A different subset of the data and a unique set of features are used to train each decision tree. In order to make a prediction, all of the decision trees' predictions are averaged to provide the final prediction.

## 3. How did you select variables to be included in the model?
After Removing all those variables which were colinear, I selected those variables which had basic colinearity with Fraud. I also used my basic knowledge of the domain and deduced variables using feature importance analysis.

## 4. Demonstrate the performance of the model by using best set of tools.
I have used 2 models i.e. Decision Tree Model and Random Forest Model and there scores are given below and as we can see both have a similar accuracy. Although Random Forest Model has a better Precision but Decision Tree has a better Recall and F1 Score.



* Decision Tree
    Accuracy: 0.9993202485768441

    Precision: 0.7909686817188638

    Recall: 0.6526442307692307

    F1 score: 0.7151794534079684

* Random Forest

    Accuracy: 0.9992094451656708

    Precision: 0.9686609686609686

    Recall: 0.40865384615384615

    F1 score: 0.5748098055790363

Random Forest will be a better Model for the prediction of Fraudulent customers.

## 5. What are the key factors that predict fraudulent customer
* Time of the Transaction

* Amount/Amount Transferred

* Type of Transaction

* Already Flagged Fraud

## 6. Do these factors make sense? If yes, How? If not, How not?
These factors make sense since they align with established patterns of fraud. For instance, fraudulent transactions are frequently done at odd hours and for large sums of money. This model can recognize these trends and correctly forecast fraudulent transactions.

## 7. What kind of prevention should be adopted while the company updates its infrastructure?
Companies can take a number of preventative measures to reduce fraud, including installing multifactor authentication, real-time transaction monitoring, and the use of machine learning models to identify and flag questionable transactions. Regular security protocol updates and training for staff and customers on fraud prevention best practices are also crucial.

* Use only intelligent vertified apps.
* Visit websites that have been safeguarded.
* Use VPNs to connect to the internet securely.
* Update the security on your laptop and mobile device.
* Don't reply to unauthorised calls, SMSes, or emails.
* Contact your bank right away if you believe your security has been violated or you have been duped.

## 8. Assuming these actions have been implemented, how would you determine if they work?
* Monitoring the number of flagged transactions.
* Bank sending E-statements.
* Customers keep a check of their account activity.
* Keep inquiring with customers on every bank transaction.
