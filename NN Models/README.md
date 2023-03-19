使用神经网络的初衷是希望通过复杂的网络结构从量价数据中自行挖掘因子;  

从IC和ICIR来看, 1d CNN效果最好; LSTM次之, DNN再次之;  

从分层效应来看, LSTM和DNN好于1d CNN;   

对比原始数据的IC均值, 所有神经网络均有所提升, 且发现LSTM严格优于DNN;  

所有模型效果均不如lightGBM和hybrid模型

由于模型文件较大, 故不上传github。有需要可联系2434722850@qq.com获取
