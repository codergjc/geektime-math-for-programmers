# 19 | 概率和统计：编程为什么需要概率和统计？

一些必备的基础概念：

- 随机变量（Random Variable）：描述事件所有可能出现的状态
  - 离散型随机变量（Discrete Random Variable）
    - 联合概率 P(x, y) 在 y 上面求和，可以得到 P(x)，这就是边缘概率（Marginal Probability），可以帮我们去除那些我们不需要关心的事件，把联合概率转换为非联合概率，忽略 y 事件的影响
  - 连续型随机变量（Continuous Random Variable）
- 概率分布（Probability Distribution）：每个状态出现的可能性
- 联合概率：两个随机变量联合起来才能决定

其实概率论研究的就是这些概率之间相互转化的关系，比如联合概率、条件概率和边缘概率。通过这些关系，概率论中产生了著名的贝叶斯定理（Bayes’ theorem）。加上变量的独立性，我们就可以构建朴素贝叶斯（Naive Bayes）分类算法，这个算法在机器学习中的应用非常广泛，我们后面也会有一节课专门来讲。

基于概率发展而来的信息论也有很多概念：

- 信息熵（Entropy）/香农熵（Shannon Entropy）
- 信息增益（Information Gain）
- 基尼指数（Gini）

这些都被用到了决策树（Decision Tree）的算法中。

## 概率和统计

概率和统计其实是互逆的。概率论是对数据产生的过程进行建模，然后研究某种模型所产生的数据有什么特性。而统计学正好相反，它需要通过已知的数据，来推导产生这些数据的模型是怎样的。因此统计特别关注数据的各种分布、统计值及其对应的统计意义。

#### 应用

- 算法复杂度计算
- 机器学习

机器学习中的监督式学习，就是通过训练样本，估计出模型的参数，最后使用训练得出的模型，对新的数据进行预测。通过训练样本来估计模型，我们可以交给统计来完成。在机器学习的特征工程步骤中，我们可以使用统计的正态分布，标准化（standardization）不同取值范围的特征，让它们具有可比性。

此外，对机器学习算法进行效果评估时，AB 测试可以减少不同因素对评测结果的干扰。为了获得更可靠的结论，我们需要理解统计意义，并为每个 AB 测试计算相应的统计值。

最后，概率模型从理论上对某些机器学习算法提供了支持。朴素贝叶斯分类充分利用了贝叶斯定理，使用先验概率推导出后验概率，并通过变量之间相互独立的假设，把复杂的计算进行大幅的简化。简化之后，我们就可以把这个算法运用在海量文本的分类任务上。

## 思考题

Q：概率统计的认识？觉得最难的是什么？
A：表示某件事情发生的概率，然后就是复合概率之间的各种概率运算，最后得出做某件事情的指导建议。最难的是抽象问题计算概率，然后概率之间的计算。
