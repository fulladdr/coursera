# Backpropagation

**Question 1**

You are training a three layer neural network and would like to use backpropagation to compute the gradient of the cost function.  In the backpropagation algorithm, one of the steps is to update
delta(2)ij = delta(2)ij + delta(3)i*(a(2)0j
 for every i, ji,j.  Which of the following is a correct vectorization of this step?


**Solution**

delta(2) = delta(2)+delta(3)*a(2)T is correct, as it takes the outer product of two vectors.


**Question 2**

Suppose \tt{Theta1}Theta1 is a 5x3 matrix, and \tt{Theta2}Theta2 is a 4x6 matrix. You set \tt{thetaVec = [Theta1(:) ; Theta2(:)]}thetaVec=[Theta1(:);Theta2(:)].  Which of the following correctly recovers \tt{Theta2}Theta2?


**Solution**

reshape(thetaVec(16:39),4,6). Since Theta1 has 15 elements, so Theta2 begins at index 16 and ends at 16+24-1


**Question 3**

Let J(\theta) = 2 \theta^4 + 2J(θ)=2θ 4+2.  Let \theta=1θ=1, and \epsilon = 0.01ϵ=0.01.  Use the formula \frac{J(\theta + \epsilon) - J(\theta - \epsilon)}{2\epsilon} 2ϵJ(θ+ϵ)−J(θ−ϵ) to numerically compute an approximation to the derivative at \theta=1θ=1.  What value do you get? (When \theta = 1θ=1, the true/exact derivative is \frac{dJ(\theta)}{d\theta} = 8 dθdJ(θ) =8.)


**Solution**

8.0008 is correct, since {(2*(1.01)^4+2)-(2*(0.09)^4+2)}/(2*0.01)=8.0008


**Question 4**

Which of the following statements are true? Check all that apply.
1. Using a large value of \lambdaλ cannot hurt the performance of your neural network; the only reason we do not set \lambdaλ to be too large is to avoid numerical problems.

2. Using gradient checking can help verify if one's implementation of backpropagation is bug-free.

3. If our neural network overfits the training set, one reasonable step to take is to increase the regularization parameter \lambdaλ

4. Gradient checking is useful if we are using gradient descent as our optimization algorithm.  However, it serves little purpose if we are using one of the advanced optimization methods (such as in fminunc).


**Solution**

2. True. If the gradient computed by backpropagation is the same as one computed numerically with gradient checking, this is very strong evidence that you have a correct implementation of backpropagation

3 . True. Just as with logistic regression, a large value of \lambdaλ will penalize large parameter values, thereby reducing the changes of overfitting the training set.


**Question 5**

Which of the following statements are true? Check all that apply.

1. Suppose that the parameter \Theta^{(1)}Θ (1)is a square matrix (meaning the number of rows equals the number of columns).  If we replace \Theta^{(1)}Θ (1) with its transpose (\Theta^{(1)})^T(Θ (1)) T, then we have not changed the function that the network is computing.

2. Suppose we have a correct implementation of backpropagation, and are training a neural network using gradient descent.  Suppose we plot J(\Theta)J(Θ) as a function of the number of iterations, and find that it is increasing rather than decreasing.  One possible cause of this is that the learning rate \alphaα is too large.

3. If we are training a neural network using gradient descent, one reasonable "debugging" step to make sure it is working is to plot J(\Theta)J(Θ) as a function of the number of iterations, and make sure it is decreasing (or at least non-increasing) after each iteration.

4. Suppose we are using gradient descent with learning rate \alphaα.  For logistic regression and linear regression, J(\theta)J(θ) was a convex optimization problem and thus we did not want to choose a learning rate \alphaα that is too large.  For a neural network however, J(\Theta)J(Θ) may not be convex, and thus choosing a very large value of \alphaα can only speed up convergence.

**Solution**

2, 3 is true. 
2 is true, because if the learning rate is too large, the cost function can diverge during gradient descent. Thus, you should select a smaller value of \alphaα.


3. is true, since gradient descent uses the gradient to take a step toward parameters with lower cost (ie, lower J(\Theta)J(Θ)), the value of J(\Theta)J(Θ) should be equal or less at each iteration if the gradient computation is correct and the learning rate is set properly.