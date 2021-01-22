function f()---g()

gradient descent(几个参数偏微分几次)
1、model y=b+w*Xcp 
2、w1=  w0-learning wight(dL/dw)|w=w0  learning wight---data update rate,learning rate
 (graduate liner Dont't worry about the difference of the result,
because the liner data alaways have the same result in the liner.)
3、if b=-188.4 w=2.7（通过偏微分学习得到）
此时把所有的点画出来，即得到回归曲线（training data）
average error on Training data （即每个点到回归曲线竖直的平均距离e1~e10）



How is the result?Generalization？what we really care about is ther error on new data?(testing data)
没见过新的，误差是多少这才是重点

How can we do better?We need a new model,select another model
引入二次式y=b+w1*Xcp+W2*Xcp2(比如说在初始的几个值是非常不准的)

b=-10.3 w1=1.0 w2=0.0027
Testing考虑平方后error会更低一些

......Slightly better.How about more complex model?可以继续加平方
（有可能越多会导致错误，就是training average error不错，但是testing的average error的很差）
所以training error会随着function复杂而降低，testing就不一定了
（A more Complex model does not always lead to better performance on testing data.This is Overfitting） 
model并不是越复杂越好
......
There are hidden factors(比如宝可梦不同物种不一样)

so let's redesign the model物种不同Model不一样
y=b1*冲激函数（Xs=pidgey）+w1*冲激函数(Xs=Pidgey)Xcp
+b2*冲激函数（Xs=weedle）+w2*冲激函数(Xs=weedle)Xcp
+...
+...
冲激函数可以根据IF，不同物种选择不同的模型，这样可以仍然保持Liner，线性关系
这样的training data的线有好几条，因为不同物种线不同

Are there any other hidden factor?把想得到的因素都加进去，比如在刚刚的原式后再加上体重、生命值、身高等参数
把无用的参数删去可以避免overfitting

Back to step2:regularization.

Loss（Loss越小说明function越好）:error： L=（连加yn-(b+连加wixi)2）2    +娜姆大(手调) 连加 wi2 
The functions with smaller Wi are better输入变化时候 输出不敏感，避免受到noises的影响
