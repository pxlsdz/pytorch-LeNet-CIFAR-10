# 项目介绍

本项目采用pytorch实现了LeNet网络，应用CIFAR-10数据集图片分类。

## 数据集介绍

CIFAR-10 数据集由 10 个类别的 60000 张 32x32 彩色图像组成，每个类别有 6000 张图像。 有 50000 张训练图像和 10000 张测试图像。10个类别分别为:'plane', 'car', 'bird', 'cat', 'deer','dog', 'frog', 'horse', 'ship', 'truck'。

下载地址： https://www.cs.toronto.edu/~kriz/cifar-10-python.tar.gz，或直接允许本项目代码就可以下载。

## 代码逻辑

1.使用torchvision加载并预处理CIFAR-10数据集
2.定义LeNet网络
3.定义损失函数和优化器
4.训练网络并更新网络参数
5.测试网络 

## 代码运行

本文的代码类型为ipynb文件，可在本地的JupyterNotebook或者在云端Notebook实验平台运行如[cloab](https://colab.research.google.com/notebooks/intro.ipynb?utm_source=scs-index)，[Mo](https://mo.zju.edu.cn/)

## Requirement

- python3.6+
- numpy
- pytorch1.8.1+cuda
- torchvision0.9.0

## 超参数分析示例

本项目选用学习率为实验对象，设置不同的学习率：[0.1, 0.05, 0.01]（因为资源和时间限制），探究不同学习率对模型的影响。不同学习率的迭代次数增加的损失率如下图：

![下载 (1)](README.assets/%E4%B8%8B%E8%BD%BD%20(1).png)

随着迭代次数的增加，模型的损失一直在减少，说明模型已经学习到一定内容。有图中可见，如果学习速率α太小，梯度下降收敛速度会很慢；如果学习速率α太大，损失函数的值在每次迭代后不一定能下降，算法最后可能会发散。对于学习速率α，可以先选择0.001，然后按10倍来进行调整 。





