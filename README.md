# CreditCard_Fraud_Detection
This project uses python and machine learning to find fraudulent credit card transactions in a dataset of 284,807 transactions where only 492 (0.17%) were fraud cases. First, we carefully checked the data and found no missing information, but noticed that most transactions (99.83%) were legitimate while very few (0.17%) were fraudulent. To fix this imbalance, we made a new balanced dataset that kept all 492 fraud cases and randomly picked an equal number of normal transactions.

We prepared the data by cleaning and standardizing all the features (V1-V28 columns, transaction Amount, and Time) using StandardScaler. Then we trained a Logistic Regression model with special settings: we adjusted the class weights to handle the imbalance, used the LBFGS solver with up to 5000 iterations, and set a fixed random state to get consistent results.

The model worked very well, showing 91.4% accuracy on test data and 95.6% on training data, which means it learned properly without overfitting. When we checked its performance in detail, we found it could detect fraud with 95% precision (correctly identifying fraud when it predicted fraud) and 88% recall (finding most actual fraud cases). For normal transactions, it had 89% precision and 95% recall. Both fraud and legitimate transactions got equal F1-scores of 91%, showing balanced performance.

Our analysis revealed fraud transactions average $122 versus $88 for legitimate ones. The solution effectively handles data imbalance while maintaining strong detection.  
