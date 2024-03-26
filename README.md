Introduction

An anonymous startup company that provides machine learning solutions in the European Banking Market is interested in developing a robust machine learning algorithm from call center information predicting high success outcomes and having interpretability for clients to make informed decisions.  Calls are made out to customers selling subscriptions to term loan deposits.  Customers are aware that they can only withdraw their funds once their agreed term (ranging from 1 month to 3 years) comes to an end.  Information is collected from the customers in a survey.

Data Description

The data is tabulated with 12 columns and 1 target variable with 40000 rows.  The following attributes are listed below:

age : age of customer (numeric)
job : type of job (categorical)
marital : marital status (categorical)
education (categorical)
default: has credit in default? (binary)
balance: average yearly balance, in euros (numeric)
housing: has a housing loan? (binary)
loan: has personal loan? (binary)
contact: contact communication type (categorical)
day: last contact day of the month (numeric)
month: last contact month of year (categorical)
duration: last contact duration, in seconds (numeric)
campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)

Structure

1. After importing modules, three machine learning functions were defined; logistic regression, decision tree and random forest.  These are the machine learning algorithms that were used for the project.
2. The data was read and the target variable distribution of classes was visualized.  The class distribution of the dataset is imbalanced with less than 10% in the positive class.
3. The data was cleaned and processed with some columns replaced with dummy variables for machine learning algorithms and converting some columns of data from categorical to numerical.
4. Correlations were visualized to ensure all variables are independent of one another.  Any independent variable with higher correlations were removed until correlations show complete independence.
5. The data was split up into a training set and a test set (40% test) used at the end to evaluate the success of the algorithm.
6. The training data was tested using all three algorithms with high accuracy but low ROC score.  The problem with the low ROC score is because of imbalanced distribution of classes so the algorithm is not sensitive enough to correctly classify more positives.  So the classes need to be balanced before the algorithms can work.
8. Three methods of balancing out the classes of the target variable were used; Random sampling with replacement, SMOTE (synthetic minority oversampling technique) and ADASYN (adaptive synthetic sampling).  The same training data was used for all three methods.
9. The test data was used to evaluate the accuracy and ROC score of the algorithm used all methods made a significant improvement using this method.

Conclusion

Random sampling with replacement, SMOTE and ADASYN were all effective methods at balancing out class data enabling machine learning algorithms to perform more accurately with higher ROC scores.  The best algorithm came from a random forest from treating the training data with SMOTE.  Of all the variables, duration was the strongest determining variable and was used to create a decision tree classifier with an 80% accuracy score and a 73% ROC score.
