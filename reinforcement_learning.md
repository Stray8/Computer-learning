# Machine Learning

## Definition 

​	A computer program is said to learn from experience E with respect to some task T and some performance measure P, if its performance on T, as measured by P, improves with experience E.

+ Experience E
+ task T
+ performance measure P

## Category 

+ Supervised Learning

  Notation

  + m: the number of training examples
  + x: input variable / features
  + y: output variable / target variable
  + (x, y) : one training example
  + (x^(i), y^(i)) : the i training example
  + h: hypothesis, map from x to y 

  different problem

  + Regression problem--predict real-valued outputs
    + Linear Regression

  + Classification problem--predict discrete-valued outputs 
    + Logistic Regression
  
  
  cost function(代价函数)--J
  
  Gradient descent
  
  + Gradient descent alogrithms
  
    Feature Scaling
  
    ​	Get every feature into approximately a [-1, +1]  range.
  
    Learning rate
  
    + rate is too small: slow convergence
    + rate is too large: cost function may not decrease on every iteration and may not converge.
  
  + Normal Equation Method


+ Unsupervised Learning

## Reinforcement Learning

### different from other machine learning

+ No supervised, Only a reward signal
+ feedback is delay
+ Time really matters

### Reward, Action, Observation
