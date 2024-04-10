# <span style="color:#4285F4;">Online Payment Fraud Detection Model Card</span>

Our model is designed to analyse online payment transactions to detect potential fraud. By examining features like transaction amounts, account balances before and after transactions, and the timing of these activities, it applies a combination of machine learning techniques to predict fraudulent behavior. This model utilises statistical analysis and classification algorithms, including RandomForest and DecisionTree classifiers, optimised through methods like GridSearchCV, BayesSearchCV and RandomizedSearchCV, to identify patterns indicative of fraud. Its performance is evaluated based on accuracy, precision, recall, and the area under the precision-recall curve, providing a comprehensive understanding of its effectiveness in distinguishing between legitimate and fraudulent transactions. This analytical approach allows for enhanced security in online financial activities by identifying and flagging suspicious transactions.

<img src="/images/precision-Recall-Curve.png" alt="Performance Graph" width="500"/>

*Graph showing model performance across various metrics.*


## MODEL DESCRIPTION
<img src="/images/fraudDetectionIcon.jpg" alt="Model Icon" width="300"/>


**Input:** Describe the inputs of your model
The model inputs include various features from a financial dataset, specifically focusing on online payment transactions. These features include,
- step: maps 1 hour of time
- type of transaction
- transaction amount
- customer who started the transaction
- account balances before and after the transactions
- customer who is the recipient of the transaction
- recipient balances before and after the transactions

**Output:** Describe the output(s) of your model
- Binary classification: `0` for legitimate, `1` for fraudulent

**Model Architecture:** Describe the model architecture you’ve used
The analysis employs multiple machine learning models, including RandomForestClassifier and DecisionTreeClassifier, optimised via GridSearchCV, BayesSearchCV and RandomizedSearchCV. A significant part of the analysis involves feature importance analysis, hypothesis testing for predictor significance, and stacking classifiers for improved prediction accuracy.


## <span style="color:#4285F4;">Performance</span>
Give a summary graph or metrics of how the model performs. Remember to include how you are measuring the performance and what data you analysed it on. 

The model's performance is evaluated using accuracy, precision, recall, and the area under the precision-recall curve (PR AUC). Performance metrics are provided for RandomForestClassifier and DecisionTreeClassifier, with additional insights from confusion matrices and precision-recall curves. The model demonstrates high accuracy in fraud detection, with further details on performance metrics such as the model accuracy score, which reflects the model's effectiveness in classifying fraudulent transactions.

| Model                                | Accuracy (%) | Precision | Recall | F1-Score | PR AUC | ROC AUC |
|--------------------------------------|--------------|-----------|--------|----------|--------|---------|
| Logistic Regression (GridSearchCV)   | 99.89        | 1         | 1      | 1        | 0.02   | 0.92    |
| RandomForest (BayesSearchCV)         | 99.93        | 1         | 1      | 1        | 0.6    | 0.96    |
| RandomForest (RandomizedSearchCV)    | 99.93        | 1         | 1      | 1        | 0.57   | 0.89    |
| DecisionTree (GridSearchCV)          | 99.91        | 1         | 1      | 1        | 0.43   | 0.88    |
| Stacked Model                        | 99.9         | 1         | 1      | 1        | 0.54   | 0.95    |


## <span style="color:#4285F4;">Limitations</span>
- **Data Imbalance**: The dataset contains a much higher proportion of non-fraudulent transactions compared to fraudulent ones, potentially biasing the model.
- **Feature Selection**: The removal of certain features based on hypothesis testing could overlook complex interactions between variables that might be predictive of fraud.
- **Generalisation**: The model's performance on data outside the provided dataset is uncertain, especially concerning different types of online payment fraud.


## <span style="color:#4285F4;">Trade-offs</span>
- **Complexity vs. Interpretability**: Advanced models like stacked classifiers offer improved accuracy but at the cost of interpretability, making it harder to understand the model's decision-making process.
- **Sampling Strategy**: Addressing the data imbalance through under-sampling or over-sampling techniques can improve model sensitivity to fraud cases but may also increase the false positive rate.
- **Feature Engineering**: The choice to simplify the model by removing features or combining categories within features can improve model manageability but may reduce the overall predictive power.

