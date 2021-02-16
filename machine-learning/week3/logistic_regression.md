#Logistic Regression

**Question 1**

Suppose that you have trained a logistic regression classifier, and it outputs on a new example x a prediction hθ(x) = 0.7. This means (check all that apply)

+ Our estimate for P(y=1|x;θ)P(y=1∣x;θ) is 0.3.
+ Our estimate for P(y=1|x;θ)P(y=1∣x;θ) is 0.7.   
+ Our estimate for P(y=0|x;θ)P(y=0∣x;θ) is 0.3.   
+ Our estimate for P(y=0|x;θ)P(y=0∣x;θ) is 0.7.   


**Solution**

Estimate for P(y=1|x;θ) is 0.7, so estimate for P(y=0|x;θ) is 0.3


**Question 2**

Suppose you have the following training set, and fit a logistic regression classifier hθ(x)=g(θ0+θ1x1+θ2x2). Which of the following are true? Check all that apply.

+ Adding polynomial features (e.g., instead using h(x)=g(0+1x1+2x2+3x12+4x1x2+5x22) ) could increase how well we can fit the training data

+ The positive and negative examples cannot be separated using a straight line. So, gradient descent will fail to converge

+ At the optimal value ofθ (e.g., found by fminunc), we will haveJ(θ)≥0

+ Because the positive and negative examples cannot be separated using a straight line, linear regression will perform as well as logistic regression on this data.

**Solution**

1. True. Adding polynomial features can only improve fitness of the data.

2. False. It is true Positive and negative examples cannot be separated by a straight line, but gradient descent will still converge to the optimum.

3. True. Cost function of J has always non-negative result.

4. False. This data is for classification, not prediction which means linear regression will not perform as well as logistic regression on the data.

**Question 4**

Which of the following statements are true? Check all that apply.

+ For logistic regression, sometimes gradient descent will converge to a local minimum (and fail to find the global minimum).  This is the reason we prefer more advanced optimization algorithms such as fminunc (conjugate gradient/BFGS/L-BFGS/etc).  

+ Linear regression always works well for classification if you classify by using a threshold on the prediction made by linear regression.

+ The cost function J(θ) for logistic regression trained with m \geq 1m≥1 examples is always greater than or equal to zero. 

+ The sigmoid function g(z) = \frac{1}{1 + e^{-z}}g(z)= 1+e −z1 is never greater than one ( >1 >1).   

+ Since we train one classifier when there are two classes, we train two classifiers when there are three classes (and we do one-vs-all classification).  

**Solution**

- False. The cost function for logistic regression is convex, so gradient descent will ALWAYS converge to global minimum.

- False. Linear regression often doesn't work well for classification.

- True. Since the cost function is a summation over the cost for each example.

- True. Sigmoid function is never bigger than one.

- False. We need 3 classifiers when there are 3 classes.