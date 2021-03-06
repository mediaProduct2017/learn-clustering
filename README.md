# learn-clustering

[kmeans](https://github.com/arfu2016/nlp/tree/master/nlp_models/kmeans)

Clustering往往是多维数据分析的第一步。

K means clustering的优化目标是使类间距离最大，类内距离最小。类间距离用各个类平均点之间距离的平均值来代表，叫做a，类内距离用类内各个点距该类平均点之间的距离的平均值来代表，叫做b，这样的话，优化目标就是让b/a达到最小，或者是让b-a达到最小。

在K means clustering的具体算法中，先随机选k个点（k是superparameter，选择k时，可以用validation data来看b/a或者b-a），把其余点分配在这k个类中（按与这k个点的距离最近者来分），然后重新计算各个类的中心（该类各点的平均值），也计算各个点到各个类中心的距离，把点重新分配到k个类中，不断重复以上过程，直到结果收敛，也就是每个点的类别都不再发生变化。
