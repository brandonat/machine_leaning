# Machine Learning Notes
May 12, 2016  

### Different Approaches
  
Probabilistic Based  
- Naive Bayes
  

```r
library(e1071)
naiveBayes(formla, data, laplace = TRUE, ...)
## option 'Laplace = TRUE' is very useful with lots of zero values.
## It works by adding a small amount to each zero so that the overall
##   pictures doesn't appear as zero.
```
  
Information-Based  
- Random Forests
  

```r
library(randomForest)

tuneRF(...) 
## Tells you how many trees you should use.
## Works by determining whether adding a tree provides a meaningful
##   improvement. Somewhat simplistic in that it doesn't consider
##   the benefit from more than one tree added.
```
  
Error Based  
- Support Vector Machines (SVM)  
- Logistic Regression with Regularization  


```r
library(kernlab) ## SVM

library(glmnet)
cv.glmnet(...) ## ridge + lasso
predict(..., s = c(lambda_min, lambda_se), ...)
```
  
### Evaluation  
  
- Accuracy  
- AUC/ROC  
- Type 1 errors  
- Sensitivity/Specificity  
- TPR/FPR  
- Kappa (result is %improvement over a coinflip)  
  

```r
library(caret)
confusionMatrix(...) ## runs eval metrics
```
