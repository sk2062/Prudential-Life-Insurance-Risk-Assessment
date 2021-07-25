# Prudential-Life-Insurance-Risk-Assessment

PROBLEM STATEMENT:

  1.Underwriting Life Insurance is an antiquated and a laborious process. The insurance firms need to conduct intensive research and risk assessment of the customers before offering any products. The entire process takes over a month on average. As a result, Life Insurance statistics among US adults are below par. People need the right product but also a speedy and a convenient process.

  2.So, the motivation behind the project is to develop a predictive model that accurately classifies risk with a more automated approach using machine learning multi-classification algorithms. Accurate risk assessment is very important for the insurance firms, since the downside risk is extremely large in case, they misclassify the customer.

  3.Additionally, by performing advanced data analytics as done in the project, the firms can make it quicker and less labor intensive for new and existing customers to get an insurance quote while maintaining privacy boundaries.Lastly, enabling the process to be significantly streamlined using existing data points and assessment.

Data Analysis and approach used:

Performed exploratory data analysis and based on the results two approaches were followed to develop a model.

  Approach 1: Used Principal Component Analysis to reduce the number of features to 120, which explain the 99% of variance explained. However, with PCA the features become less interpretable and later on we cannot refine the features used in the model.

  Approach 2: Kept the same number of features to maintain the interpretability. Removed highly correlated and variables with low variance. As a result used 702 columns to build the models.
  
  Results: 
  
  # Results with Approach 1(PCA):
    Models used          CV score     Test Accuracy
    Naive Bayes              0.4055      0.3955
    Logistic regression    0.4796      0.4666
    Decision Trees          0.4284      0.4277
    Random Forests       0.4732      0.4602
    Gradient Boosting     0.4567      0.4355

  # Results with Approach 2(Without PCA):
    Models used           CV score      Test Accuracy
    Naive Bayes              0.3793      0.3798
    Logistic regression    0.4519      0.4469
    Decision Trees          0.5031      0.5046
    Random Forests       0.5000      0.4978
    Gradient Boosting     0.5004      0.4838

  For Approach 1, Logistic Regression gives the best results.
  For Approach 2, Decision Trees gives the best results.
  Cross-Validation and Hyperparameter tuning done using RandomizedSearchCV and GridSearchCV.
  For ensemble methods, oob_score is used for cross validation.
