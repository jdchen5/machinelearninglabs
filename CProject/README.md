# PROJECT TITLE 


## NON-TECHNICAL EXPLANATION OF YOUR PROJECT
100 words to explain what your project is about to a general audience. 

Our model acts as a digital detective, trained to distinguish between regular online payment transactions and potentially fraudulent ones. It scrutinises each transaction's details—such as the money involved, the account's historical balance, and the transaction's origin or destination — to determine its legitimacy. Utilising advanced algorithms, akin to a detective piecing together clues from a crime scene, the model predicts whether a transaction is genuine or if it's an attempt at fraud. This process helps safeguard online financial activities, ensuring users' transactions are secure and trustworthy. By analysing patterns from vast amounts of data, the model learns to identify the subtle signs of fraud that might escape the human eye, making it an essential tool in the fight against digital financial crimes.


## DATA
A summary of the data you’re using, remembering to include where you got it and any relevant citations. 

We used a dataset that contains information on hundreds of thousands of online transactions, including whether they were fraudulent or not. This data includes details like the amount of money involved, the accounts sending and receiving the money, and when the transactions took place. The dataset was generously made available by Kaggle, and you can find it here. [https://www.kaggle.com/datasets/pankajtiwari2003/fraudlent-transaction]


## MODEL 
A summary of the model you’re using and why you chose it. 

This modesl serve as the brain of our digital detective, interpreting complex data to make smart decisions swiftly. We employ multiple machine learning models, including RandomForestClassifier and DecisionTreeClassifier, optimised via GridSearchCV, BayesSearchCV, and RandomizedSearchCV. Decision Tree model was chosen for its transparency in decision-making, which is crucial for establishing trust when managing financial transactions. 

A significant part of the analysis involves feature importance analysis, hypothesis testing for predictor significance, and stacking classifiers to improve prediction accuracy. All chosen models excel in classification tasks.


## HYPERPARAMETER OPTIMSATION
Description of which hyperparameters you have and how you chose to optimise them. 

Hyperparameters are like the settings on a detective's toolkit, adjusting how thorough or quick the investigation is. We utlised various methods such as BaySearchCV and RandomizedSearchCV, which systematically tries out different combinations of settings to find the optimal ones. This ensures our digital detective is not only smart but also efficient, using its resources wisely to catch fraudsters.

RandomForestClassifier (BayesSearchCV): to grow a magical forest where the trees are classifiers that help us decide between different choices
- 'max_depth'= 11: plant our trees with a certain depth (11 layers of branches)
- 'min_samples_leaf' = 1: each leaf has at least one piece of information before making a decision
- 'min_samples_split' =  10: split the branches when we have at least 10 pieces of information
- 'n_estimators' = 143: to grow 143 trees in our forest



## RESULTS
A summary of your results and what you can learn from your model 

Our model proved to be quite the sleuth in identifying fraudulent transactions. It could accurately spot a high percentage of frauds, significantly reducing the risk for everyone involved. We learned that even though no model is perfect, with the right data and settings, we can greatly minimize the threat of online payment fraud. Below is an example plot showing our model's accuracy:

You can include images of plots using the code below:
![Screenshot](image.png)


## (OPTIONAL: CONTACT DETAILS)
If you are planning on making your github repo public you may wish to include some contact information such as a link to your twitter or an email address. 

If you're interested in learning more about our project or have suggestions for improvements, feel free to reach out or follow our work on GitHub at [Your GitHub Repo Link]. For direct inquiries or collaboration opportunities, email us at [your_email@example.com].

