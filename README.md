# Model-for-predicting-the-wine-variety-.
# Name : SK SAMEERUDDIN
# Mail ID : SHAIK.18BCD7140@VITAP.AC.IN

# Introduction

In the below, I will test the ability of various classifiers at predicting a certain wine variety from UCI's dataset. The idea is to single out a particular wine variety (class 1) and attempt to identify it from the other 2 classes, using a small selection of predictor variables from the data set.

For the purposes of this notebook, I was less interested in the importance of variable selection and more interested in the relative performance of the different classifiers, using the same variables. Hence, I have picked just 2 predictor variables (alcohol and flavanoids content) and evaluated models on the basis of accuracy and other metrics from the confusion matrices such as Sensitivity, Specificity and Precision.

# The classifiers I have compared are:

Logistic Regression (for an example of a model which provides a predictability score and has options for tuning parameters)
Support Vector Machine (for an example of a strong linear classifier applied to an "almost linearly separable" scenario)
Decision Tree (for an example of a non-parametric learner)
AdaBoost ensemble method (for an example of an ensemble method of weak learners)
Multi-Layer Perceptron (for an example of a neural network model more suited to high-dimensional, non-linear examples)
Summary
The results for the optimized models are as follows:

# Confusion Matrix Metrics

Logistic Regression - Accuracy:=0.92958, Sensitivity:=0.81818, Specificity:=0.97959, Precision:=0.94737
Support Vector Machine - Accuracy:=0.98592, Sensitivity:=1.00000, Specificity:=0.97959, Precision:=0.95652
Decision Tree - Accuracy:=0.95775, Sensitivity:=0.86364, Specificity:=1.00000, Precision:=1.00000
AdaBoost ensemble - Accuracy:=0.95775, Sensitivity:=0.86364, Specificity:=1.00000, Precision:=1.00000
Multi-Layer Perceptron - Accuracy:=0.98592, Sensitivity:=0.95455, Specificity:=1.00000, Precision:=1.00000
Cross Validated Accuracy

Logistic Regression - Cross Validated Accuracy:= 0.91667 +/- 0.09044
Support Vector Machine - Cross Validated Accuracy:= 0.92778 +/- 0.07049
Decision Tree - Cross Validated Accuracy:= 0.91667 +/- 0.10015
AdaBoost ensemble - Cross Validated Accuracy:= 0.92222 +/- 0.10000
Multi-Layer Perceptron - Cross Validated Accuracy:= 0.95556 +/- 0.05443
Logistic Regression performed worst overall, having the lowest scores on all confusion matrix metrics and a cross-validated accuracy that was joint worst with the Decision Tree.

The Decision Tree and the AdaBoost ensemble performed identically. This makes sense given that the AdaBoost ensemble uses Decision Trees as base classifiers.

The SVM achieved the joint highest test accuracy and out-performed the Logistic Regression model on all scores, except for tying with Specificity.

The MLP was more specific and precise than the SVM but less sensitive and they both had the same test accuracy. However, the cross-validated accuracy for the MLP is greater and had fairly low variance.

The MLP was the best performing model, overall, and we may expect this, given that the classes are not perfectly linearly separable and the neural network is more suited to non-linear classification tasks.
