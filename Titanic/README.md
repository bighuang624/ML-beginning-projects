# Titanic 

### 第一次提交

在探索数据后，我决定选用以下特征进行预测`'Pclass', 'Sex', 'Age', 'Embarked', 'SibSp', 'Parch', 'Fare'`。其中 Age、Embarked 和 Fare 有缺失，考虑使用出现频率最高的值来填充 Embarked 特征（类别型）的缺失值，使用平均值来填充 Age 和 Fare 特征（数值型）的缺失值。而类别特征不能直接作为输入，因此采用 DictVectorizer 对特征抽取和特征向量化。

最后使用 RandomForest 分类器来进行预测。Public Score 为 0.73205。

### 第二次提交

Fare 只有一个缺失，而 Age 存在 86 个缺失值。因此，直接使用平均值来填充 Age 的缺失值可能对预测结果影响较大。我将 Age 从选取的有效特征中剔除，其他不变，Public Score 提高到 0.75598。

### 第三次提交

在对别人分享的 kernel 进行学习后，这次我做了比较详细的特征工程（具体操作在下一节），并且进行了 sklearn 中常用分类器效果的比较，最终选用了 SVC 分类器。本次的 Public Score 提高到 0.80861。