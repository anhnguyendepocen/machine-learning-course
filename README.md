## Introduction

This is the R equivalent version of all assignments of the online machine learning course (MOOC) offered by Stanford university and instructed by [Andrew NG](http://www.andrewng.org). The course materials including lectures and presentation PDFs, can be downloaded all at once from [Coursera website](https://class.coursera.org/ml-003/lecture). 

One can accomplish the assignment and quizzes and earn a certificate from [Coursera](https://www.coursera.org/learn/machine-learning), although the assignments MUST be submitted in Octave/Matlab still. R submission is not yet supported. This repository is the first step to bring this excellent online course to the great community of R users.

The code provides the starter code and infrastructure for carrying out the assignment in R statistical software. The completed assignments are available too, however publishing the solutions is against the course rules. If you had any question regarding the assignments, fill free to ask them here in Github issues.

To accomplish the assignments simply fill the parts of the code that is written "Your Code HERE". The assignment instructions (pdf) are included in this repository also. There is a RStudio project file in each exercise folder that is a proper starting point to complete the codes.

## Dependencies (3rd party packages)
I have tried my best not to use a 3rd party package in the starter codes. However to produce similar results and plots to Octave/Matlab I had to use a few packages although they are not many. 

[rgl](https://cran.r-project.org/package=rgl) package is used to produce the 3D scatter plots and surface plots in the exercises.

There are many optimization tasks within the assignments. Most of them that are not large scale optimization problem and they were optimized using built-in `optim` function of R. However to solve optimization problems in exercise 4 and exercise 8, I have used a slightly modified version of [lbfgsb3](https://cran.r-project.org/package=lbfgsb3) package. One should first install the package and then source the `lbfgsb3_.R` file. The sourcing is done in the starter codes automatically. `fmincg` or `fminunc` optimization functions in Octave/Matlab take one function as input that calculates cost and gradient simultaneously. However cost and gradient functions MUST be supplied into `optim` or `lbfgsb3` functions individually. So I have separated the cost and gradient functions in the starter codes.

Stemmer software (portStemmer.m) is used in the exercise 6 (spam classification) and the `portStemmer` function is called from `processEmail` function. Instead of re-implementing `portStemmer` function in R, I have used [SnowballC](https://cran.r-project.org/package=SnowballC) package that produces the same results as with the case of portStemmer.m.

`R.matlab` package was used for reading Octave/Matlab `.mat` datasets. The datasets were converted to `.Rda`  format. Thus you would not need this package to complete the exercise.

Last but not the least is the Octave/Matlab `pinv` function. There is a `ginv` function in `MASS` package that doesn't produce the same exact result of `pinv`. Therefore a slightly modified version of MASS `ginv` is included in the starter codes. `MASS` package is not needed to be installed.

To wrap up, before starting to code make sure the following 3 packages are installed: `rgl`, `lbfgsb3`, `SnowballC`.

## Screen-shots
A few screenshots of the plots produced in R:

![](https://github.com/faridcher/faridcher.github.io/blob/master/ml-course/Snapshots/AnomolyDetection.png)

## Topics covered in the course and assignments
1. Linear regression, cost function and normalization
2. Gradient descent and advanced optimization
3. Multiple linear regression and normal equation
4. Logistic regression, decision boundary and multi-class classification
5. Over-fitting and Regularization
6. Neural Network non-linear classification
7. Model validation, diagnosis and learning curves
8. System design, prioritizing and error analysis
9. Support vector machine (SVM), large margin classification and SVM kernels (linear and Gaussian)
10. K-Means clustering
11. Principal component analysis (PCA)
12. Anomaly detection, supervised learning
13. Recommender systems, Collaborative filtering
14. Large scale machine learning, stochastic and mini-batch gradient descent, online learning, map reduce


## License
This work is licensed under a [Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/)
[https://github.com/faridcher/faridcher.github.io/blob/master/ml-course/Snapshots/AnomolyDetection.png]: https://github.com/faridcher/faridcher.github.io/blob/master/ml-course/Snapshots/AnomolyDetection.png