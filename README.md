# Introduction
This project trains two different models and finds out which model performs better. I perform classification of apples quality. I found this data set on Kaggle and just wanted to do simple ML project. We will use a logistic regression model and a support vector machine model.

## What did I do?
First I looked into the data. It had several features size, weight, Sweetness, Crunchiness, Juiciness, Ripeness, Acidity, Quality. Then i performed little bit of EDA. I looked into the basic statistics of the data like mean, std, quartiles etc. I looked for any null values. Then I looked into the correlation data by making a correlation matrix. Finally I compared the features of the mean data of the two classes using bar plot. Mean values of size, sweetness, juiciness and ripeness seems to be the most varied.

Then I removed the null values and added class labels for the quality output 0 for bad and 1 for good. Then Split the data into test and train 80% train and 20% test. 

Then I trained the models.

For Logistic regression I used liblinear solver with l2 regularization. Then I trained the model.

For Support vector machine I used the default vanilla configuration and train the model.

I created confusion the matrix for both of them. 

## Observation 
Looking at confusion matrix we can easily see the support vector machine has better performance overall. When we look at their accuracy logistic regression has about 74% accuracy compared to 88% accuracy of SVM. But accuracy doesn't tell us the full story so we also look at the other metrics like precision, recall etc. But even in those metrics SVM blows logistic regression out of water. So, overall for this SVM is better suited model. The reason might be SVM being able to separate non-linearly separable data. As we are using RBF kernel for the SVM which supports non-linear relationships unlike plain old linear regression.

## Future work 
Well looks like SVM is a better model here. But I can still make improvements. Here I am simply using simple train test split. I can move on to cross validation. Also I can use learning curves and validation curves to select right amount of data and right value of the parameters.
