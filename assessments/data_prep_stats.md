### Question 1

Using the `pandas` library, how would you read a .csv file into a DataFrame, including an argument for the column names?

A. `pd.read_csv('filename', names=column_names)`  **(Correct)**
B. `pd.read_csv('filename', axis=column_names)`
C. `open('filename', 'r')`
D. `pd.read_csv('filename', axis=1)`

### Question 2

What are the steps to load a locally saved filed into a Colab notebook and assign it to a DataFrame? Assume your local file is named `data.csv`.

A. **(Correct)**
```
1.
`from google.colab import files`
`uploaded = files.upload()`
2.
Click 'browse' to select the file to upload.
3.
`import io`
`df = pd.read_csv(io.BytesIO(uploaded['data.csv']))`
```

B. `pd.read_csv('data.csv')`

C.
```
url = 'http://localfile_location'
pd.read_csv(url)
```

D.
```
`file = open("data.csv", "r")`
`df = pd.read_csv(file)`
```

### Question 3

The *tidy data* format is best described as	a format where
A. each variable is a column and each observation is a row.  **(Correct)**
B. a format where each observation is a column and each variable is a row.
C. formatted data that doesn't contain any NaN or Null values
D. data where all columns in a table or DataFrame are of the same data type.

### Question 4

If you wanted to join two data frames (`df1`, `df2`) along a column named "student_id", and only include the rows that share a common key (the column being joined on), which of the following choices is correct?	

A. `pd.merge(df1, df2, on='student_id', how='inner')`  **(Correct)**
B. `df1.merge(how='inner')`
C. `pd.merge(df1, df2, on='student_id', how='outer')`
D. `df1.concat(df2, on='student_id')`

### Question 5

How would you apply a custom function called `myfunction` to "col1" of your DataFrame df ?

A. `df['col1'].apply(myfunction)`  **(Correct)**
B. `df.apply(myfunction)`
C. `df.apply(column='col1', function=myfunction)`
D. `pd.apply(df['col1'], myfunction)`

### Question 6

Which of the following statement is **not** true of outliers in a dataset?

A. Outliers should always be removed from data before conducting any analses. **(Correct)**
B. Outliers are points that lie away from the bulk of the rest of the data.
C. Outliers can indicate errors in the data.
D. Outliers can indicate unusual but correct data.


### Question 7

Which of the following correctly identifies the null and alternative hypotheses for a one-sample t-test?

A. Ho: mu = reference value  vs. Ha: mu != reference value  **(Correct)**
B. Ho: mu != reference value  vs. Ha: mu = reference value
C. Ho: mu = t-statistic  vs. Ha: mu != t-statistic
D. Ho: mu = reference value  vs. Ha: mu = t-statistic

### Question 8

We conduct a hypothesis test and get a p-value of 0.02, which of the following is true at the alpha = 0.05 significance level?

A. We reject the null hypothesis and conclude the alternative is true. **(Correct)**
B. We fail to reject the null hypothesis and prove that it is true.
C. It depends on the value of the t-statistic.
D. It depends on the number of degrees of freedom.

### Question 9

Which is a correct statement of the Central Limit Theorem?

A. The Central Limit Theorem tells us that, regardless of the distribution of a single observation, as long as the sample size is large enough (about 30-40), the distribution of the sample mean will be Normal with a mean equal to the mean of the original distribution. **(Correct)**

B. The Central Limit Theorem tells us that, regardless of the distribution of a single observation, as long as the sample size is large enough (about 30-40), the distribution of the sample mean will be Chi-square with a mean equal to the mean of the original distribution.

C. The Central Limit Theorem tells us that, regardless of the distribution of a single observation, as long as the sample size is large enough (about 300-400), the distribution of the sample mean will be Normal with a mean equal to the mean of the original distribution.

D. The Central Limit Theorem tells us that, regardless of the distribution of a single observation, as long as the sample size is large enough (about 30-40), the distribution of an individual observation will be Normal with a mean equal to the mean of the original distribution.

### Question 10

Which of the following correctly identifies the null and alternative hypotheses for a chi-square test?

A. Ho: The two variables are not associated with each other vs. Ha: The two variables are associated with each other  **(Correct)**
B. Ho: The two variables are associated with each other vs. Ha: The two variables are not associated with each other
C. Ho: mu = reference value  vs. Ha: mu != reference value
D. Ho: u != reference value  vs. Ha: mu = reference value

### Question 11

You would like to compare the mean height of cherry tomato plants grown using an industrial fertilizer to the mean height of cherry tomato plants grown using organic fertilizer. What type of test are you conducting when comparing the means of samples from these two populations?

A. 2-sample t-test **(Correct)**
B. 1-sample t-test
C. 35-sample t-test
D. dependent samples t-test

### Question 12

Which of the following choices best describes a situation where conditional probability is considered?

A. The probability that a passenger survived the Titanic sinking given that the passenger was male. **(Correct)**
B. The probability that a passenger survived the Titanic sinking and was male.
C. The probability that a passenger survived the Titanic sinking.
D. The probability that a passenger was male.

### Question 13

What is the difference between a linear correlation of 1 and a linear correlation of -1?

A. A linear correlation of 1 is positive, meaning as the independent variable increases, the dependent variable also increases. A linear correlation of -1 is negative meaning as the independent variables increases the dependent variable decreases. **(Correct)**

B. A linear correlation of 1 is positive, meaning as the independent variable increases, the dependent variable also increases. A linear correlation of -1 is negative meaning as the independent variables increases the dependent variable decreases.

C. A linear correlation of 1 is *negative*, meaning as the independent variable increases, the dependent variable also increases. A linear correlation of -1 is *positive* meaning as the independent variables increases the dependent variable decreases. 

D. These linear correlations are the same; the sign is used just as a convention.

### Question 14


We have a linear relationship described by the following equation:

`y = 0.32 + 0.063x`

We want to make a prediction for x=3; what is the value of y?
A. 0.509 **(Correct)**
B. 0.189
C. 0.32
D. We can't use this equation to make a prediction.

### Question 15

When we fit a linear regression and determine the slope is essentially zero, do we reject or fail to reject the null hypothesis?

A. We **fail to reject** the null hypothesis; there is no relationship between variables where the linear regression slope coefficient is zero. **(Correct)**
B. We **reject** the null hypothesis; there is no relationship between variables where the linear regression slope coefficient is zero.
C. A hypothesis test isn't appropriate to use in this situation.
D. There is no null hypothesis for a slope coefficient of zero so we can neither eject or fail to reject.

### Question 16

The 95% confidence interval for a slope coefficient of 5.8578 is [4.006, 7.709]. What would change about this interval if the confidence level was decreased to 90%?

A. The confidence interval would be *narrower* because we would be *less* certain of the true value of the slope.  **(Correct)**
B. The confidence interval would be *wider* because we would be *less* certain of the true value of the slope.
C. The confidence interval would be *wider* because we would be *more* certain of the true value of the slope.
D. The confidence interval would remain the same.

### Question 17

Which of the following choices is the best description of the R-squared value?

A. It is a statistical measure of the proportion of variance for a dependent variable that's explained by an independent variable(s). **(Correct)**
B. It is a measure of the accuracy of the prediction.
C. It is a measure of the residual for a specific pair of dependent-independent variables.
D. It is a measure of the error in the slope and intercept of the best-fit line for two variables in a linear regression model.

### Question 18

If two vectors have exactly the same length, will they also have a cosine similarity equal to 1?

A. No. Vectors with the same length can point in different directions; the cosine similarity would not necessarily be equal to 1. **(Correct)**
B. Yes. Vectors with the same length will always have a cosine similarity equal to 1.
C. Not enough information. We need to know more about the dimensions of the vectors before we can determine the value for cosine similarity.
D. We can't calculate the cosine similarity for only two vectors so the value for cosine similarity doesn't exist.

### Question 19

When representing a linear regression with multiple independent variables using the matrix format, how many columns will the **X** matrix have? Assume the regression will include determining the intercept.

A. The number of columns will be equal to 1 plus the number of independent variables. **(Correct)**
B. The number of columns will be equal to the number of data points used in the regression model.
C. The number of columns is always equal to two, no matter how many variables are used in the regression.
D. The number of columns is equal to the number of target variables.
