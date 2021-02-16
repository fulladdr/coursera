# Regularization

**Question 1**
Which of the following statements are true? Check all that apply.

+ The activation values of the hidden units in a neural network, with the sigmoid activation function applied at every layer, are always in the range (0, 1). 

+ Suppose you have a multi-class classification problem with three classes, trained with a 3 layer network. Let a(3)1=(hΘ(x))1 be the activation of the first output unit, and similarly a(3)2=(hΘ(x))2 and a(3)3=(hΘ(x))3. Then for any input x, it must be the case that a(3)1+a(3)2+a(3)3=1

+ Any logical function over binary-valued (0 or 1) inputs  x1 and x2 an be (approximately) represented using some neural network.

+ A two layer (one input layer, one output layer; no hidden layer) neural network can represent the XOR function

**Solution**

+ True. If sigmoid activation function is applied, values are always in the range (0,1)

+ False. It can be the case, but it is not a must.

+ True. Since logical function composes of AND, OR, and negation, which we can build using two layer network, any logical function can be represented.

+ False. XOR function needs at least three layers.

**Question 2**
Consider the following neural network which takes two binary-valued inputs x1,x2∈{0,1} and outputs hΘ(x). Which of the following logical functions does it (approximately) compute?

**Solution**
Since hΘ(x) = g(-30+20x1+20x2),
when x1=0, x2=0 hΘ(x)=g(-30)~=0,
when x1=0, x2=1 hΘ(x)=g(-10)~=0,
when x1=1, x2=0 hΘ(x)=g(-10)~=0,
when x1=1, x2=1 hΘ(x)=g(10)~=1

So the answer is AND

**Question 3**
Consider the neural network given below. Which of the following equations correctly computes the activation a1(3)? Note: g(z) is the sigmoid activation function.

**Solution**
Since a1(3) is dealing with layer3, inside the g function should be values dealing with layer2. So we can eliminate the second option.
Also, a1(3) is first object of layer3, theta should be starting with 1, which eliminates option 4. 
Theta should be from layer 2, which also eliminates option 1. 
