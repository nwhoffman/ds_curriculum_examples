### Question 1

Which *one* of the following would NOT make a good starting baseline for a machine learning model:

A. A neural network. **(Correct)**
B. A simple linear regression.
C. A logistic regression.
D. The most common class in the dataset (for a classification model).

### Question 2

Consider the following processes:

* Principal Component Analysis (PCA)
* One-hot encoding
* Extracting additional date information from a single date format

What type of process are they all describing?

A. feature engineering **(Correct)**
B. model evaluation
C. model training
D. exploratory data analysis

### Question 3

Using the following example of a data set `(X, y)` and implementing a train/test split, what are the shapes of the `X_train` and `y_train` sets? Read lines 9-10 carefully.

```python
1  import numpy as np
2  from sklearn.model_selection import train_test_split
3
4  X = np.array([[1, 4], [2, 6], [4, 6], [7, 8], [1, 9],
5             [3, 7], [6, 1], [9, 6], [9, 8], [1, 7]])
6
7  y = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
8
9  X_train, X_test, y_train, y_test = train_test_split(
10             X, y, test_size=0.2, random_state=42)
```

A. `X_train`= (8,2) and `y_train` = (8,) **(Correct)**
B. `X_train`= (2,2) and `y_train` = (0,2)
C. `X_train`= (10,2) and `y_train` = (0,20)
D. `X_train`= (42,10) and `y_train` = (0,42)

### Question 4

Suppose you have a pandas column named `color` with the following values: `cyan, cyan, magenta, yellow, magenta`.

How would the above series of labels be one-hot encoded for the `color_cyan` label

A. 1, 1, 0, 0, 0 **(Correct)**
B. 2
C. 0, 0, 1, 1, 1
D. 0, 1

### Question 5

For the following regression equation, where *p* is the probability of predicting a class given `X`, what do the coefficients Beta_0 and Beta_1 represent?

*Hint: Think about the form of the right-hand side of the equation below: if you plotted it, would it be a straight line or something else?*

```
p(X) = exp(Beta_0+Beta_1*X) / 1 + exp(Beta_0+Beta_1*X)
```

A. The coefficients of a *logistic regression* where Beta_0 is the intercept and Beta_1 is the change of p(X) with a one unit change in `X` **(Correct)**
B. The coefficients of a *linear regression* where Beta_0 is the intercept and Beta_1 is the change of p(X) with a one-unit change in `X`
C. The coefficients of a *logistic regression* where Beta_0 is the intercept and Beta_1 is the slope or average change in p(X) with a one-unit change in `X`
D. The coefficients of a *linear regression* where Beta_0 is the intercept and Beta_1 is the slope or average change in p(X) with a one-unit change in `X`

### Question 6

Using the scikit-learn pipeline steps shown below, what is the type of model being fit and what type of encoding is being used?

```python
model = pipeline.named.steps['logisticregression']
encoder = pipeline.named.steps['onehotencoder']
encoded_columns = encoder.transform(X_val).columns
coefficients = pd.Series(model.coef_[0], encoded_columns)
```

A. A logistic regression using one-hot encoding. **(Correct)**
B. A logistic regression without any encoding.
C. A linear regression with categorical encoding.
D. A logistic regression using coefficients for encoding.

### Question 7

Given the following confusion matrix, which choice shows the correct accuracy?

|               | Predicted: No | Predicted: Yes |
|-------------|---------------|----------------|
| Actual: No | 45            | 50             |
| Actual: Yes | 10            | 100          |

A. accuracy = 71% **(Correct)**
B. accuracy = 10%
C. accuracy = 45%
D. accuracy = 100%

### Question 8

Refer to the following image and choose the answer that best describes what is being illustrated:

![u2_s2_scikit_learn_kfold.png](https://raw.githubusercontent.com/LambdaSchool/data-science-canvas-images/main/sprint_assessment/u2_s2_scikit_learn_kfold.png)"

A. Cross-validation with five splits and five folds **(Correct)**
B. Cross-validation with five splits and no folds
C. Cross-validation with 25 folds (5x5)
D. A model evaluation technique that isn't possible to implement.

### Question 9

Which of the following model evaluation techniques are most suitable for a *regression model*? **Choose one answer only.**

A. Mean square error (MSE) or root mean square error (RMSE) **(Correct)**
B. Receiver operating characteristic (ROC) curve
C. Accuracy
D. Precision

### Question 10

You are creating a classification model and check to see how your classes are distributed, you find that the majority class occurs 61% of the time. When it's time to evaluate your model, is it reasonable to use the accuracy score (correct predictions/total predictions)?

A. Yes. Because the classes are relatively balanced, the accuracy score is a reasonable estimate for the results of your model. **(Correct)**
B. Yes but only because all classification models can be reasonably evaluated using the accuracy score.
C. No. The accuracy score isn't a good option for evaluating any classification model, because the scoring metric is too simplistic.
D. In this case, we need more specific information about the classification model in order to know if we can use the accuracy score.

### Question 11

You are creating a classification model and check to see how your classes are distributed, you find that the majority class occurs 61% of the time. When it's time to evaluate your model, is it reasonable to use the accuracy score (correct predictions/total predictions)?

A. Yes. Because the classes are relatively balanced, the accuracy score is a reasonable estimate for the results of your model. **(Correct)**
B. Yes but only because all classification models can be reasonably evaluated using the accuracy score.
C. No. The accuracy score isn't a good option for evaluating any classification model, because the scoring metric is too simplistic.
D. In this case, we need more specific information about the classification model in order to know if we can use the accuracy score.

### Question 12

What is occuring when information from outside the training set is used to train a model?

A. feature leakage **(Correct)**
B. feature selection
C. feature engineering
D. feature importance

### Question 13

If we permute a feature and determine it doesn't change the accuracy of our prediction, should we continue to use that feature in our model?

A. No. By permuting the features we can determine which ones are most important to keep. **(Correct)**
B. Yes. Even if permuting the feature doesn't change the model accuracy, we should always retain all of our features.
C. Yes. Permuting features is only useful for calculating the final model accuracy and not feature selection.
D. No. After a feature is permuted, it is no longer useful to keep in the model.

### Question 14

What does the term "gradient" mean when used in "gradient boosting"?

A. It is a boosting technique that makes use of a gradient descent method when adding trees to the boosted model. **(Correct)**
B. A gradient is how features are selected during the feature permutation process in boosting.
C. The gradient refers to how the accuracy is measured in a boosted model.
D. The gradient is used to determine the number of trees to add to the boosted model.

### Question 15

What is an advantage of using partial dependence plots to interpret models?

A. They provide more information for how individual features impact model predictions. **(Correct)**
B. They are a superior method than simple feature importance rankings.
C. They increase the accuracy of our model predictions.
D. They provide a robust way to detect if leaky features are being used in our models.
