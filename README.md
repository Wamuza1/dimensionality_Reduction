# Dimensionality_Reduction

# Project Overview

Many ML problems involves thousabds or more than that features for each trainaing instance. These features make training slow and make harder to find a good solution. It helps to speed up training process and also useful for data viz. it make it easy and plot a condensed view of a high dimensional traing set on a graph and provide us insightful visualization.

# Purpose

In this project we will examin the two popular dimensionality reduction algorithms.
- PCA
- LDA


# PCA vs LDA: What to Choose for Dimensionality Reduction?
In case of uniformly distributed data, LDA almost always performs better than PCA. However if the data is highly skewed (irregularly distributed) then it is advised to use PCA since LDA can be biased towards the majority class.

Finally, it is beneficial that PCA can be applied to labeled as well as unlabeled data since it doesn't rely on the output labels. On the other hand, LDA requires output classes for finding linear discriminants and hence requires labeled data.


In the script above the LinearDiscriminantAnalysis class is imported as LDA. Like PCA, we have to pass the value for the n_components parameter of the LDA, which refers to the number of linear discriminates that we want to retrieve. In this case we set the n_components to 1, since we first want to check the performance of our classifier with a single linear discriminant. Finally we execute the fit and transform methods to actually retrieve the linear discriminants.

Notice, in case of LDA, the transform method takes two parameters: the X_train and the y_train. However in the case of PCA, the transform method only requires one parameter i.e. X_train. This reflects the fact that LDA takes the output class labels into account while selecting the linear discriminants, while PCA doesn't depend upon the output labels.
