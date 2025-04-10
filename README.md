# Classification-Models
Build and evaluate various ML classification models using Python.

## 1. Logistic Regression Classification

Logistic regression is a classification algorithm, used when the value of the target variable is categorical in nature. Just like Linear regression assumes that the data follows a linear function, Logistic regression models the data using the sigmoid function. As it happens, a sigmoid function, defined as follows, produces output having those same characteristics and thus ensures that the model output always falls between 0 and 1:

Based on the number of categories, Logistic regression can be classified as:

+ **Binomial:** target variable can have only 2 possible types: “0” or “1” which may represent “win” vs “loss”, “pass” vs “fail”, “dead” vs “alive”, etc.
+ **Multinomial:** target variable can have 3 or more possible types which are not ordered(i.e. types have no quantitative significance) like “disease A” vs “disease B” vs “disease C”.
+ **Ordinal:** it deals with target variables with ordered categories. For example, a test score can be categorized as:“very poor”, “poor”, “good”, “very good”. Here, each category can be given a score like 0, 1, 2, 3.

## 2. Decision Tree Classification

A Decision Tree is a simple representation for classifying examples. It is a Supervised Machine Learning where the data is continuously split according to a certain parameter.
Decision Tree consists of :

+ **Nodes :** Test for the value of a certain attribute.
+ **Edges/ Branch :** Correspond to the outcome of a test and connect to the next node or leaf.
+ **Leaf nodes :** Terminal nodes that predict the outcome (represent class labels or class distribution).

## 3. Random Forest Classification

The Random Forest Classifier is a set of decision trees from randomly selected subset of training set. It aggregates the votes from different decision trees to decide the final class of the test object. It is an ensemble tree-based learning algorithm. 

#### Ensemble Algorithm :
Ensemble algorithms are those which combines more than one algorithms of same or different kind for classifying objects. For example, running prediction over Naive Bayes, SVM and Decision Tree and then taking vote for final consideration of class for test object.

## 4. K-nearest neighbour Classification

K-nearest neighbors (KNN) algorithm is a simple, easy-to-implement supervised machine learning algorithm that can be used to solve both classification and regression problems.

The KNN algorithm assumes that similar things exist in close proximity. In other words, similar things are near to each other. KNN captures the idea of similarity (sometimes called distance, proximity, or closeness) with some mathematics we might have learned in our childhood— calculating the distance between points on a graph.

For finding closest similar points, you find the distance between points using distance measures such as Euclidean distance, Hamming distance, Manhattan distance and Minkowski distance. Euclidean distance is a popular and familiar choice. KNN has the following basic steps:

+ Calculate distance
+ Find closest neighbors
+ Vote for labels

## 6. Naive Bayes Classification

Naive Bayes is a statistical classification technique based on Bayes Theorem. It is one of the simplest supervised learning algorithms. Naive Bayes classifier is the fast, accurate and reliable algorithm. Naive Bayes classifiers have high accuracy and speed on large datasets.

Naive Bayes classifier assumes that the effect of a particular feature in a class is independent of other features. Bayes theorem provides a way of calculating probability

+ **P(h):** the probability of hypothesis h being true (regardless of the data). This is known as the prior probability of h.
+ **P(D):** the probability of the data (regardless of the hypothesis). This is known as the prior probability.
+ **P(h|D):** the probability of hypothesis h given the data D. This is known as posterior probability.
+ **P(D|h):** the probability of data d given that the hypothesis h was true. This is known as posterior probability.

# Model evaluation

### Classification accuracy

Accuracy is one metric for evaluating classification models. Informally, accuracy is the fraction of predictions our model got right.

For binary classification, accuracy can also be calculated in terms of positives and negatives.

Where TP = True Positives, TN = True Negatives, FP = False Positives, and FN = False Negatives.

Accuracy alone doesn't tell the full story when you're working with a **class-imbalanced data set**, where there is a significant disparity between the number of positive and negative labels. Metrics for evaluating class-imbalanced problems are precision and recall.

### Confusion matrix

A confusion matrix is a tool for summarizing the performance of a classification algorithm. A confusion matrix will give us a clear picture of classification model performance and the types of errors produced by the model. It gives us a summary of correct and incorrect predictions broken down by each category. The summary is represented in a tabular form.

Four types of outcomes are possible while evaluating a classification model performance. These four outcomes are described below:-

+ **True Positives (TP)** – True Positives occur when we predict an observation belongs to a certain class and the observation actually belongs to that class.
+ **True Negatives (TN)** – True Negatives occur when we predict an observation does not belong to a certain class and the observation actually does not belong to that class.
+ **False Positives (FP)** – False Positives occur when we predict an observation belongs to a certain class but the observation actually does not belong to that class. This type of error is called Type I error.
+ **False Negatives (FN)** – False Negatives occur when we predict an observation does not belong to a certain class but the observation actually belongs to that class. This is a very serious error and it is called Type II error.

### Classification Report
Classification report is another way to evaluate the classification model performance. It displays the precision, recall, f1 and support scores for the model. 

#### Precision
Precision can be defined as the percentage of correctly predicted positive outcomes out of all the predicted positive outcomes. It can be given as the ratio of true positives (TP) to the sum of true and false positives (TP + FP).

So, Precision identifies the proportion of correctly predicted positive outcome. It is more concerned with the positive class than the negative class.

Mathematically, precision can be defined as the ratio of TP to (TP + FP).

#### Recall
Recall can be defined as the percentage of correctly predicted positive outcomes out of all the actual positive outcomes. It can be given as the ratio of true positives (TP) to the sum of true positives and false negatives (TP + FN). Recall is also called Sensitivity.

Recall identifies the proportion of correctly predicted actual positives.

Mathematically, recall can be given as the ratio of TP to (TP + FN). True Positive Rate is synonymous with Recall and can be given as the ratio of TP to (TP + FN).

#### f1-score
f1-score is the weighted harmonic mean of precision and recall. The best possible f1-score would be 1.0 and the worst would be 0.0. f1-score is the harmonic mean of precision and recall. So, f1-score is always lower than accuracy measures as they embed precision and recall into their computation. The weighted average of f1-score should be used to compare classifier models, not global accuracy.
