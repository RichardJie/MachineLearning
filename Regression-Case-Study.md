function f()---g()

gradient descent(��������ƫ΢�ּ���)
1��model y=b+w*Xcp 
2��w1=  w0-learning wight(dL/dw)|w=w0  learning wight---data update rate,learning rate
 (graduate liner Dont't worry about the difference of the result,
because the liner data alaways have the same result in the liner.)
3��if b=-188.4 w=2.7��ͨ��ƫ΢��ѧϰ�õ���
��ʱ�����еĵ㻭���������õ��ع����ߣ�training data��
average error on Training data ����ÿ���㵽�ع�������ֱ��ƽ������e1~e10��



How is the result?Generalization��what we really care about is ther error on new data?(testing data)
û�����µģ�����Ƕ���������ص�

How can we do better?We need a new model,select another model
�������ʽy=b+w1*Xcp+W2*Xcp2(����˵�ڳ�ʼ�ļ���ֵ�Ƿǳ���׼��)

b=-10.3 w1=1.0 w2=0.0027
Testing����ƽ����error�����һЩ

......Slightly better.How about more complex model?���Լ�����ƽ��
���п���Խ��ᵼ�´��󣬾���training average error��������testing��average error�ĺܲ
����training error������function���Ӷ����ͣ�testing�Ͳ�һ����
��A more Complex model does not always lead to better performance on testing data.This is Overfitting�� 
model������Խ����Խ��
......
There are hidden factors(���籦���β�ͬ���ֲ�һ��)

so let's redesign the model���ֲ�ͬModel��һ��
y=b1*�弤������Xs=pidgey��+w1*�弤����(Xs=Pidgey)Xcp
+b2*�弤������Xs=weedle��+w2*�弤����(Xs=weedle)Xcp
+...
+...
�弤�������Ը���IF����ͬ����ѡ��ͬ��ģ�ͣ�����������Ȼ����Liner�����Թ�ϵ
������training data�����кü�������Ϊ��ͬ�����߲�ͬ

Are there any other hidden factor?����õ������ض��ӽ�ȥ�������ڸոյ�ԭʽ���ټ������ء�����ֵ����ߵȲ���
�����õĲ���ɾȥ���Ա���overfitting

Back to step2:regularization.

Loss��LossԽС˵��functionԽ�ã�:error�� L=������yn-(b+����wixi)2��2    +��ķ��(�ֵ�) ���� wi2 
The functions with smaller Wi are better����仯ʱ�� ��������У������ܵ�noises��Ӱ��
