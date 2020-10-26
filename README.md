# PoC-Predicting-Employee-Turnover
Employee turnover is very costly for organizations. Organizations such as consulting firms would suffer from deterioration in customer satisfaction 
due to regular changes in Account Reps and/or consultants that would lead to loss of businesses with clients.

This project is to build a classifier that help a client company predict employee turnover and reduce costs (such as recruitment, training, 
and replacement and so forth) which are caused by employee turnover.

Machine learning classification tools are advantageous data mining techniques to predict future employee behaviours (performance and attrition probabilities) 
based on past data trends. Based on the Human Resources past employee data mining and analysis, it is possible to predict future behaviours in the organization.

-Data Preprocessing

There are some data preprocessing needed:
Change sales feature name to department.
Convert salary into ordinal categorical feature since there is intrinsic order between: low, medium and high.

-Feature Engineering

Create dummy features from department feature and drop the first one to avoid linear dependency where some learning algorithms may struggle.

-Building Training/Test Data

We have an imbalanced dataset. We use the below two method:
Assign a larger penalty to wrong predictions from the minority class.
Upsampling the minority class or downsampling the majority class.

-Model Selection

We use the most common 5 classifiers: Random Forest, Gradient Boosting Trees, K-Nearest Neighbors, Logistic Regression and Support Vector Machine.
For model selection, we follow:
- Build a pipeline that includes two steps (standardizing the data and calling the classifier we want to use to fit the model) when fitting the classifier.
- Use GridSearchCV to tune hyperparameters using 10-folds cross validation.
- Fit the model with the best hyperparameters using training data.
- Plot ROC curves and calculate recall、f1 scores to evaluate models using test data.

-Model Evaluation

The performance matrixs are utilized for evaluating models are: f1 score, auc, and ROC curve.

-Featuren Importance

Since Random Forest and Gradient Bossting Trees have the best performance, we see their feature importance.
