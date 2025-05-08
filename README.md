# credit-risk-classification

## Summary

Within this challenge, I used logistic regression to run statistical analysis on how well the supervised machine learning model could predict the outcome of the loan variables being tested, health vs high-risk loans. Like most regression models, I split my data into X and y variables, but rather than a simple two column data set that I could assign as the X and y variables, I grouped the data into a 'feature' (X) and 'target' (y) labels. The y variable usually consists of one column of interest where as the X variable consists all the other columns, excluding the y variable. 

In order to get the data set into the X and y variables, I created two datasets under the X and y df label to only include the columns of interest. Once those variables have been established, I used the train test split function to further split the new X and y data sets to utilize in the logistical regression model. This is just simply establishing X and y train and test variables to match the train test split function.

Once I have done that, I then fit the new data set into the logistic regression model by using the logisticregression function. Specifically I fit the model using the X and y train variables with a random state of 1 (this ensures that the splitting of the data is equal every time).

Lastly, after setting the model has been fit, I created a new variable using the  the X_test variable to make a predition, to be then implimented in the confusion matrix for the model. This matrix provides statistical insight on the performace of the data by breaking down the counts for true positives/negatives, and false positives/negatives. This is the step right before I calculated the classification (accuracy) report. This report provided even more indepth insight in the accuracy of the data set I created, better helping me conclude whether this model and data set produced accurate results. Overall, the accuracy was great.

The logistic regression model is great for datasets that are on the large side as you can group/split the data easily

## Results

|              | Precision | Recall | F1-Score | Support |
|--------------|-----------|--------|----------|---------|
|            0 | 1.00      | 0.99   | 1.00     | 18765   |
|            1 | 0.84      | 0.94   | 0.89     | 619     |
|      Accuracy|           |        | 0.99     | 19384   |
|     Macro avg| 0.92      | 0.97   | 0.94     | 19384   |
|  Weighted avg| 0.99      | 0.99   | 0.99     | 19384   |


As you can see, the accuracy for the 0 (healthy loans) and 1 (high-risk loans) weren't too bad. The total correct prediction samples to the total samples were 99% accurate. The precision rates showcase an instance in which there could be some false positives. Specifically with the high-risk label since it got an 84% precision rate versus the healthy loan with a 100%. With a lower precision, this is a good indicator of being able to identidfy true positives. Overall, the outcome of the prediction was a good model as the sample data and the true data didn't have a low accuracy percentage.

## Final Thoughts

Compared to using unsupervised learning, I think this logistic regressino model is a good option if you want to get a chart of the analysis versus a more visual output analysis. Another model I like but wouldn't use with this data set (as shown a little bit at the bottom of the coding page) is the linear regression model. Not only does this model create a nice visualization of the data, but it can also provide a statistical analysis like the classification report I created at the end. The reason I wouldn't recommend using this model is striuctly due to the fact that it's intended for linear data sets, meaning data that you can easily set the X and y variable to with respect to the columns in your dataset. Since my data set has more than two columns,I cannot easily choose which column to set as the X and y variables. I'd have to consider what I really want to compare/what makes sense to compare with only two columns.

One model I would recommend as I also utilized it in my coding workbook, is the Random Forest model. It is very simular to the Logistic Regression model, just with an extra little couple of feautures that can provide a visual aspect to the analysis. It isn't as straight forward per se one you split the data, but if one wanted to go that extra step to create a visual to go along with the newly created data set, this is a good model to utilize to help execute just that. Overall, the logistic regression model is a morer user friendly option to use than the random forest model.