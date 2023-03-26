# 首届[厚方杯](http://gdhf-inv.com/news_detail.php?CateID=11110&id=147)二等奖方案(重制版)

## 目录:  
数据分析和特征工程: [data_insight](https://github.com/HaoningChen/Houfang-Cup/blob/main/data_insight.ipynb)  
模型: [lightGBM](https://github.com/HaoningChen/Houfang-Cup/blob/main/lgbm.ipynb);  [hybrid](https://github.com/HaoningChen/Houfang-Cup/blob/main/hybrid.ipynb)  
(说明: hybrid的weight=[0, 1]时, 相当于xgboost模型; weight=[1, 0]时, 相当于线性回归模型)  
[NN Models](https://github.com/HaoningChen/Houfang-Cup/tree/main/NN%20Models): 使用神经网络进行因子挖掘, 但实际效果还是没有lgbm和hybrid好  
策略: [strategy](https://github.com/HaoningChen/Houfang-Cup/blob/main/strategy.ipynb)

## ps:  
[数据和数据说明](https://www.kaggle.com/datasets/harleychan/csi300)  
工具包: [scutquant](https://github.com/HaoningChen/ScutQuant)(v0.3.2); [qlib](https://github.com/microsoft/qlib)(v0.8.4)  
如要复现, 请下载数据后依次运行[data_insight](https://github.com/HaoningChen/Houfang-Cup/blob/main/data_insight.ipynb), [lightGBM](https://github.com/HaoningChen/Houfang-Cup/blob/main/lgbm.ipynb), [hybrid](https://github.com/HaoningChen/Houfang-Cup/blob/main/hybrid.ipynb)和[strategy](https://github.com/HaoningChen/Houfang-Cup/blob/main/strategy.ipynb)  
[tech_factors + i](https://github.com/HaoningChen/Houfang-Cup/blob/main/tech_factors%20%2B%20i.ipynb)是一个不稳定的实验版本, 主要目的是测试scutquant.alpha的技术因子。目前的因子数量还很少, 但总体而言质量还不错(尤其是与i因子的相性不错)

一个很奇怪的结论:   
将[data_insight](https://github.com/HaoningChen/Houfang-Cup/blob/main/data_insight.ipynb)中的i8因子表达式改成
$$\frac{high + low}{2 \cdot R_f \cdot close}$$
时, i8的因子质量会大幅提升, 且模型的IC也有所提升, 但使用相同的策略回测会降低$\alpha$
