# 机器人学习历程

## 一、动力学建模



## 二、最小二乘法

​		通常我们会用一组观测数据去估计模型的参数，模型是由先验知识定下的。对于一个系统的输入输出而言，存在一定的关系： 
$$
f(x)=A+BX \tag1
$$
​		但在实际应用中，我们的观测存在误差，因此我们会记录多组观测值 $(x_i,y_i)$

于是我们提出要解决的问题：求出参数的近似解，使模型在各个观测点处达到最佳"拟合"。我们通常定义**误差平方和**为模型最真实的状态，定义误差为：
$$
e_(rr)=y_i-f(x) \tag2
$$

$$
min  e_r^2
$$
