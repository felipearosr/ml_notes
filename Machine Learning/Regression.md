# Regression

A major component of machine learning involves making predictions about a target based on inputs, like predicting an individual's lifetime earnings from demographic data. This chapter focuses on predicting continuous, real numbers, a process known as regression.
## Defining the Problem

To understand regression, consider the types of problems it solves: 
1. Predicting a person's height from their parents' heights.
2. Estimating loan repayment time based on credit history.
3. Forecasting package arrival time given weather and traffic conditions.

Regression involves making predictions for continuous outputs based on given inputs. It's a class of methods used to achieve this goal, not a single technique.

> **Definition from *Undergraduate Fundamentals of Machine Learning***:
> A class of techniques that seeks to make predictions about unknown continuous target variables given observed input variables.

## Solution Options

What are the different ways that we can arrive at a solution. This is a short, non-exhaustive list of regression techniques with brief explanations:

### K-Nearest-Neighbors
K-Nearest-Neighbors is an extremely intuitive, non-parametric technique for regression or classification. It works as follows in the regression case: 
1. Identify the K points in our data set that are closest to the new data point. ‘Closest’ is some measure of distance, usually Euclidean.
2. Average the value of interest for those K data points.
3. Return that averaged value of interest: it is the prediction for our new data point.
### Neural Networks 

A neural network works by scaling and combining input variables many times. Furthermore, at each step of scaling and combining inputs, we typically apply some form of nonlinearity over our data values. The proof is beyond the scope of this textbook, but neural networks are known to be universal function approximators. This means that given enough scaling and combining steps, we can approximate any function to an arbitrarily high degree of accuracy using a neural network. 
### Random Forests
Random forests are what’s known as an ensemble method. This means we average the results of many smaller regressors known as decision trees to produce a prediction. These decision trees individually operate by partitioning our original data set with respect to the value of predictive interest using a subset of the features present in that data set. Each decision tree individually may not be a reliable regressor; by combining many of them we achieve a model with better performance.
### Gradient Boosted Trees
Gradient boosted trees are another technique built on decision trees. Assume we start with a set of decision trees that together achieve a certain level of performance. Then, we iteratively add new trees to improve performance on the hardest examples in our data set, and reweight our new set of decision trees to produce the best level of performance possible.
### Turning to Linear Regression
You’ve likely never even heard of some of these preceding techniques - that’s okay. The point is that we have a number of existing methods that take different approaches to solving regression problems. Each of these will have their own strengths and weaknesses that contribute to a decision about whether or not you might use them for a given regression problem. We obviously do not cover these methods in great detail here; what’s more important is the understanding that there are a variety of ways to go about solving regression problems. From here on out, we will take a deeper dive into linear regression. There are several reasons for which we are exploring this specific technique in greater detail. The two main reasons are that it has been around for a long time and thus is very well understood, and it also will introduce many concepts and terms that will be utilized extensively in other machine learning topics.