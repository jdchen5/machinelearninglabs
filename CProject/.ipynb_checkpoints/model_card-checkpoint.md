# Model Card

See the [example Google model cards](https://modelcards.withgoogle.com/model-reports) for inspiration. 

## Model Description

The model described is designed to analyse online payment transactions to detect potential fraud. By examining features like transaction amounts, account balances before and after transactions, and the timing of these activities, it applies a combination of machine learning techniques to predict fraudulent behavior. This model utilises statistical analysis and classification algorithms, including RandomForest and DecisionTree classifiers, optimised through methods like GridSearchCV, BayesSearchCV and RandomizedSearchCV, to identify patterns indicative of fraud. Its performance is evaluated based on accuracy, precision, recall, and the area under the precision-recall curve, providing a comprehensive understanding of its effectiveness in distinguishing between legitimate and fraudulent transactions. This analytical approach allows for enhanced security in online financial activities by identifying and flagging suspicious transactions.


**Input:** Describe the inputs of your model
The model inputs include various features from a financial dataset, specifically focusing on online payment transactions. These features include transaction amounts, account balances before and after the transaction, type of transaction, and time steps representing the transaction time.

**Output:** Describe the output(s) of your model
The model outputs a binary classification indicating whether a transaction is fraudulent (1) or not (0).

**Model Architecture:** Describe the model architecture you’ve used
The analysis employs multiple machine learning models, including RandomForestClassifier and DecisionTreeClassifier, optimised via GridSearchCV, BayesSearchCV and RandomizedSearchCV. A significant part of the analysis involves feature importance analysis, hypothesis testing for predictor significance, and stacking classifiers for improved prediction accuracy.

## Performance
The model's performance is evaluated using accuracy, precision, recall, and the area under the precision-recall curve (PR AUC). Performance metrics are provided for RandomForestClassifier and DecisionTreeClassifier, with additional insights from confusion matrices and precision-recall curves. The model demonstrates high accuracy in fraud detection, with further details on performance metrics such as the model accuracy score, which reflects the model's effectiveness in classifying fraudulent transactions.

Give a summary graph or metrics of how the model performs. Remember to include how you are measuring the performance and what data you analysed it on. 

## Limitations
Outline the limitations of your model.

* Data Imbalance: The dataset contains a much higher proportion of non-fraudulent transactions compared to fraudulent ones, potentially biasing the model.
* Feature Selection: The removal of certain features based on hypothesis testing could overlook complex interactions between variables that might be predictive of fraud.
* Generalisation: The model's performance on data outside the provided dataset is uncertain, especially concerning different types of online payment fraud.



## Trade-offs

Outline any trade-offs of your model, such as any circumstances where the model exhibits performance issues. 

* Complexity vs. Interpretability: Advanced models like stacked classifiers offer improved accuracy but at the cost of interpretability, making it harder to understand the model's decision-making process.
* Sampling Strategy: Addressing the data imbalance through under-sampling or over-sampling techniques can improve model sensitivity to fraud cases but may also increase the false positive rate.
* Feature Engineering: The choice to simplify the model by removing features or combining categories within features can improve model manageability but may reduce the overall predictive power.
