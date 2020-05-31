# Regularization

**Avoid overfitting**

**When overfitting, we often see large weights**

Idea: penalize large parameter values

## Ridge regression

**L2 regularized** linear least squares regression:

![](.gitbook/assets/76.png)

Side note L2 norm:

![](.gitbook/assets/77%20%281%29.png)

* regularization parameter  λ &gt; 0 controls the strength of regularization
* a good practice is to not penalize the intercept

## Ridge weight formula

![](.gitbook/assets/78%20%281%29.png)

## Ridge with data normalization

**Without regularization**: ![](.gitbook/assets/79.png)

![](.gitbook/assets/80.png)

**With regularization**: ![](.gitbook/assets/81%20%281%29.png)

Diff features will be penalized differently

![](.gitbook/assets/82.png)

**Instead of maximize log-likelihood, we maximize the posterior**

![](.gitbook/assets/83.png)

## Maximum a Posteriori \(MAP\)

![](.gitbook/assets/84%20%281%29.png)

## Gaussian prior

![](.gitbook/assets/85%20%281%29.png)

## Laplace prior

Lasso ![](.gitbook/assets/86%20%281%29.png)

## L1 vs L2 regularization

![](.gitbook/assets/87.png)

![](.gitbook/assets/88%20%281%29.png)

## Diff regularization subset selection

![](.gitbook/assets/89.png)

optimizing this is a diﬃcult combinatorial problem:

* search over all    2^D     subsets

## L1 VS L0

It’s just like LASSO but has a little difference. LASSO has a limit:

the L1 norm of the parameters &lt; t \(some constant threshold\)

For L0 regularization. The constraint is the number of parameters &lt; t \(some constant threshold\)

Most people never heard about it because LASSO is good enough in the cases that people want to punish some parameters to zero. L0 regularization shares the same function with it. **The difference is L0 is more extreme than L1. The parameters are much easier to be punished to zero.**

If you have 500 features in the pool and you want 10 of them left, you can try LASSO. However, if you have 10k features in the pool and you want 10 of them left, you probably want to try L0 regularization.

## Bias-variance decomposition

![](.gitbook/assets/90%20%281%29.png)

![](.gitbook/assets/91.png)

![](.gitbook/assets/92.png)

![](.gitbook/assets/93%20%281%29.png)

Larger regularization penalty -&gt; high bias – low variance

high variance in more complex models means that test and training error can be very diﬀerent

high bias in simplistic models means that training error can be high

![](.gitbook/assets/94.png)

## Cross validation

k-fold CV

![](.gitbook/assets/95%20%281%29.png)

leave-one-out CV:extreme case of k=N

Test data:

once the hyper-parameters are selected, we can use the whole set for training use test set for the **ﬁnal** assessment

## Evaluation

![](.gitbook/assets/96.png)

ROC receiver operating characteristic

![](.gitbook/assets/97%20%281%29.png)

How to graph: [https://acutecaretesting.org/en/articles/roc-curves-what-are-they-and-how-are-they-used](https://acutecaretesting.org/en/articles/roc-curves-what-are-they-and-how-are-they-used)

## 

