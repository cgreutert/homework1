<<<<<<< HEAD
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
6.”Given a voter’s profile/data, how likely is it that they will vote in
favor of the candidate?” This is an example of a predictive question
since it’s attempting to estimate the likelihood of a voter’s choice
with minimum reducible error without focusing on a hypothesis test.  
“How would a voter’s likelihood of support for the candidate change if
they had personal contact with the candidate?” This is an example of an
inferential question since it’s testing a theory that is trying to
create a causal relationship between personal contact influencing
voters’ support.

Exploratory Data Analysis  
Exercise One:

``` r
library(tidyverse)
```

    ## -- Attaching packages --------------------------------------- tidyverse 1.3.1 --

    ## v ggplot2 3.3.5     v purrr   0.3.4
    ## v tibble  3.1.6     v dplyr   1.0.7
    ## v tidyr   1.1.4     v stringr 1.4.0
    ## v readr   2.1.1     v forcats 0.5.1

    ## -- Conflicts ------------------------------------------ tidyverse_conflicts() --
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
ggplot(data = mpg) + geom_histogram(mapping = aes(x = hwy), binwidth = 1.5)
```

![](hw1_files/figure-gfm/unnamed-chunk-1-1.png)<!-- -->

I observe that most miles per gallon is under 35 mpg with a frequent
number if them being between 15-20 and 25-30 mpg. The data is mostly
right skewed and has a few outliers between 35-45 mpg.  
Exercise Two:

``` r
ggplot(data = mpg) + geom_point(mapping = aes(x = hwy, y = cty))
```

![](hw1_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

I notice a positive correlation between the highway mpg and the city
mpg. This indicates the people’s gas mileage remains roughly consistent
on the highway and in the city, if one increases, so does the other; if
one decreases, so does the other.  
Exercise Three:

``` r
library(forcats)
ggplot(mpg, aes(x=fct_infreq(manufacturer)))+ geom_bar(stat = 'count')+coord_flip()
```

![](hw1_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

Dodge produced the most cars and Lincoln produced the least.  
Exercise Four:

``` r
ggplot(data = mpg, mapping = aes(x= factor(cyl), y=hwy)) + geom_boxplot()
```

![](hw1_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

I notice that the higher the number of cylinders, the lower the miles
per gallon on the highway. I also notce that 8 cylinder cars have some
outliers that perform better on the highway. On average, 4 and 5
cylinder cars have the highest mpg.  
Exercise Five:

``` r
library("corrplot")
```

    ## Warning: package 'corrplot' was built under R version 4.1.3

    ## corrplot 0.92 loaded

``` r
corrplot(cor(mpg[ , -c(1,2,6,7,10,11)]), method = 'number', type='lower')
```

![](hw1_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

I decided to omit the categorical variables in order to calculate these
correlations. I notice a positive relationship between cty and hwy, cyl
and displ, and a negative relationship between cty and displ, hwy and
displ, cty and cyl, and hwy and cyl. These relationships make sense, a
lot of cars will have similar gas mileage in the city and on the
highway. I am surprised by the lack of relationship between highway mpg
and year.
=======
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
6.”Given a voter’s profile/data, how likely is it that they will vote in
favor of the candidate?” This is an example of a predictive question
since it’s attempting to estimate the likelihood of a voter’s choice
with minimum reducible error without focusing on a hypothesis test.  
“How would a voter’s likelihood of support for the candidate change if
they had personal contact with the candidate?” This is an example of an
inferential question since it’s testing a theory that is trying to
create a causal relationship between personal contact influencing
voters’ support.

Exploratory Data Analysis  
Exercise One:

``` r
library(tidyverse)
```

    ## -- Attaching packages --------------------------------------- tidyverse 1.3.1 --

    ## v ggplot2 3.3.5     v purrr   0.3.4
    ## v tibble  3.1.6     v dplyr   1.0.7
    ## v tidyr   1.1.4     v stringr 1.4.0
    ## v readr   2.1.1     v forcats 0.5.1

    ## -- Conflicts ------------------------------------------ tidyverse_conflicts() --
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
ggplot(data = mpg) + geom_histogram(mapping = aes(x = hwy), binwidth = 1.5)
```

![](hw1_files/figure-gfm/unnamed-chunk-1-1.png)<!-- -->

I observe that most miles per gallon is under 35 mpg with a frequent
number if them being between 15-20 and 25-30 mpg. The data is mostly
right skewed and has a few outliers between 35-45 mpg.  
Exercise Two:

``` r
ggplot(data = mpg) + geom_point(mapping = aes(x = hwy, y = cty))
```

![](hw1_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

I notice a positive correlation between the highway mpg and the city
mpg. This indicates the people’s gas mileage remains roughly consistent
on the highway and in the city, if one increases, so does the other; if
one decreases, so does the other.  
Exercise Three:

``` r
library(forcats)
ggplot(mpg, aes(x=fct_infreq(manufacturer)))+ geom_bar(stat = 'count')+coord_flip()
```

![](hw1_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

Dodge produced the most cars and Lincoln produced the least.  
Exercise Four:

``` r
ggplot(data = mpg, mapping = aes(x= factor(cyl), y=hwy)) + geom_boxplot()
```

![](hw1_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

I notice that the higher the number of cylinders, the lower the miles
per gallon on the highway. I also notce that 8 cylinder cars have some
outliers that perform better on the highway. On average, 4 and 5
cylinder cars have the highest mpg.  
Exercise Five:

``` r
library("corrplot")
```

    ## Warning: package 'corrplot' was built under R version 4.1.3

    ## corrplot 0.92 loaded

``` r
corrplot(cor(mpg[ , -c(1,2,6,7,10,11)]), method = 'number', type='lower')
```

![](hw1_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

I decided to omit the categorical variables in order to calculate these
correlations. I notice a positive relationship between cty and hwy, cyl
and displ, and a negative relationship between cty and displ, hwy and
displ, cty and cyl, and hwy and cyl. These relationships make sense, a
lot of cars will have similar gas mileage in the city and on the
highway. I am surprised by the lack of relationship between highway mpg
and year.
>>>>>>> b5ca5fe407c60f7f4bd34950a8b89fc74760e4ea
