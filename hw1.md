Homework 1: Machine Learning Main Ideas
================
Carly Greutert

1.Supervised learning involves building a model based on inputs when you
know what the output (response variable Y) is and adjusting your model
to best predict or estimate that output. Unsupervised learning, on the
other hand, has observed inputs, but no observed outputs (i.e. they do
not have a supervisor) and rely on finding trends in the inputted data
(page 26-27 in An Introduction to Statistical Learning and Lecture
One).  
2. The difference between a regression and classification model involves
the response variable Y and whether it is quantitative or qualitative
(Lecture One). In the context of machine learning, this means we are
either predicting a numerical or categorical value, regardless whether
the inputs are qualitative or quantitative.  
3. Two commonly used metrics for regression ML problems are linear and
logistic regression. Two commonly used metrics for classification
problems are Principal Component Analysis (PCA) and k-means clustering
(Lecture Two).  
4. Descriptive models chooses a model that does the best job of visually
emphasizing a data trend. One such example is graphing a line onto a
scatter plot to see correlations (Lecture Two).  
Inferential models main goal is to test theories by determining which
features are most significant (Lecture Two). Furthermore, it helps test
possible causal claims for trends in the data and “states \[the\]
relationship between outcome and predictors (Lecture Two).  
Predictive models is less concerned with hypothesis tests, unlike
inferential models. The aim is to figure out what combination of
features will help predict the response variable, Y, with minimal
reducible error (Lecture Two).  
5. Mechanistic-driven models assumes a parametric form for the function
f that takes in
*β*
predictors (
*β*<sub>0</sub> + *β*<sub>1</sub> + ... + *β*<sub>*n*</sub>
) in order to predict Y given a set of data points. It will likely not
match the actual observed response, but the goal is to limit the error
between these values. Although we can increase the flexibility of the
model since we can add parameters to create a better fit; however, if
there are too many, the data may be overfitted. In other words, the
model may be too specific based on a given sample and cannot accurately
predict other data samples (Lecture Two).  
Empirically-driven models, on the other hand, do not make any
assumptions about f. Instead, it requires a larger number of
observations to predict the response. It is similar to a
mechanistic-driven model since it is very flexible, clearly, as it is
not restricted by assumptions. This method may also be in danger of
overfitting based on your sample, also similar to mechanistic-driven
models.  
Generally speaking, mechanistic-driven models are easier to understand
because it is not as flexible, and more restricted. This increased
interpretability because it has a set of specific predictors that model
the relationship between the predictor and the response, so it is easier
to comment on how influential specific features of the model are.  
The bias-variance tradeoff describes, generally, that as we use more
flexible methods, the variance will increase and the bias will decrease.
The reverse is also true (the less flexible, variance will decrease and
bias will increase). Thus, mechanistic-driven models will tend to have
less variance and greater bias and empirically-driven models will have
greater variance and less bias(page 33-36 in An Introduction to
Statistical Learning).
