# Udacity Sparkify 项目定义

用户流失是每个软件公司不愿意看到的事情，对于音乐公司也是如此。因此，根据用户以前的数据，预测可能的流失用户，在用户注销之前提供各种可能的挽留措施，能够最大限度减少软件公司的用户损失情况。

预测流失用户，本质上是针对用户的二分类问题，因此适合采用监督学习的机器学习方法。项目主要流程包括：数据清洗，探索性分析，特征工程，监督学习建模，建模过程中采用f1分数对模型进行评估和改进。

### 使用到的库

- pandas, numpy, matplotlib
- Spark for Python - pyspark
- IBM Watson Studio

### 数据集

完整的数据集大小为12GB，由于时间和计算调价的限制，我们选取了它的一个迷你子集，大小约为几百兆，并在免费的 IBM 云平台完成大数据任务的处理和部署

### 项目流程

1. 加载数据
2. 数据清理
3. 数据的探索和可视化
4. 特征工程
    - gender(性别)
    - songsPlayed(收听歌曲次数)
    - artistsPlayed(收听作者次数)
    - thumbsUps(点赞次数)
    - thumbsDowns(点踩次数)
    - churn(标签label)
5. 建模并预测

### 项目结果

结果比较：
- LogisticRegression (best F1-score 0.767)
- RandomForestClassifier (best F1-score 0.58)

采用 `逻辑回归`, `随机森林` 两种监督学习模型，结果显示`逻辑回归` 效果更好

### 反思和改进

- 从原始数据集中提取特征到新数据集中，不破坏原始数据集
