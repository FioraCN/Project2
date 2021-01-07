# Project2
  作业背景
  
本次作业进行的讨论项目是，预测航空客流，并且以航空数乘客据为基础使用LSTM方法对短期乘客数量进行预测，并且和实际乘客数量进行对比，得到预测结果的准确性检验。
  
  算法综述
  
long short term memory，即我们所称呼的LSTM，是为了解决长期以来问题而专门设计出来的，所有的RNN都具有一种重复神经网络模块的链式形式。
递归神经网络（RNN）是两种人工神经网络的总称。一种是时间递归神经网络（recurrent neural network），另一种是结构递归神经网络（recursive neural network）。
时间递归神经网络的神经元间连接构成矩阵，而结构递归神经网络利用相似的神经网络结构递归构造更为复杂的深度网络。
RNN一般指代时间递归神经网络。
LSTM是一种特殊的RNN，主要通过三个门控逻辑实现(遗忘、输入、输出)。它的提出就是为了解决长序列训练过程中的梯度消失和梯度爆炸问题。
  
  实践结果
  
 实践的结果如图所示，预测的曲线与实际曲线比较吻合，LSTM方法预测的准确率比较高。
  
  存在的问题
  
（1）安装keras时总提示tensorflow的版本要达到2.2以上才能匹配，下载了2.4版本又找不到适配的keras版本，
    最后选择低版本tensorflow又重新安装Python3.6得以解决。
（2）数据获取比较难。轨道交通的数据不易获得且较为复杂，项目的数据因为敏感性问题不能用，所以爬取了一些较为简单容易处理的航空数据进行预测。
（3）找不到合适的其他深度学习方法。曾试过CNN，但数据量不够，预测误差较大，网上与客流预测有关的深度学习方法也找不到参考，
    最终只选用了LSTM进行了短期预测，效果较好。
