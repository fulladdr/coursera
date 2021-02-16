# Regularization

**Question 1**

You are training a classification model with logistic regression. Which of the following statements are true? Check all that apply.

+ Adding many new features to the model makes it more likely to overfit the training set

+ Introducing regularization to the model always results in equal or better performance on the training set

+ Adding a new feature to the model always results in equal or better performance on examples not in the training set

+ Introducing regularization to the model always results in equal or better performance on examples not in the training set


**Solution**

1. True. Adding many features to the model will likely to overfit the training set.

2. False. Regularization can underfit the training set and have worse performance on the training set

3. False. We cannot know what kind of features examples not in the training set have.

4. False. Regularization can underfit the training set and will not result in better performance on examples not in the training set.


**Question 2**

**Solution**

Theta that has smaller value corresponds to lambda = 1, since bigger lambda can help prevent overfitting on the training set.

**Question 3**

Which of the following statements about regularization are true? Check all that apply

+ Because logistic regression outputs values 0 \leq h_\theta(x) \leq 10≤hθ(x)≤1, its range of output values can only be "shrunk" slightly by regularization anyway, so regularization is generally not helpful for it.

+ Using a very large value of λ cannot hurt the performance of your hypothesis; the only reason we do not set λ to be too large is to avoid numerical problems.

+  Using too large a value of λ can cause your hypothesis to overfit the data; this can be avoided by reducing λ.

+ Consider a classification problem.  Adding regularization may cause your classifier to incorrectly classify some training examples (which it had correctly classified when not using regularization, i.e. when λ=0).  

**Solution**

1. False. 

2. False. We do not use too large lambda since it can lead to underfitting.

3. False. Too large value of lambda can cause hypothesis to underfit the data.

4. True. Adding regularization doesn't always guarantee better performance.

**Question 4**

In which one of the following figures do you think the hypothesis has overfit the training set?

**Solution**

1. Because it seems to fit for every examples in the graph but it is a wiggly curve and cannot guarantee it will fit for the newly introduced data.

**Question 5**

In which one of the following figures do you think the hypothesis has underfit the training set?

**Solution**

1. Because the graph is too much a simple curve and doesn't seem to fit the data.