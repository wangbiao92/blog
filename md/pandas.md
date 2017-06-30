区别(Numpy, Scipy, Pandas)
====================
- Numpy是以矩阵为基础的数学计算模块，纯数学。
- Scipy基于Numpy，科学计算库，有一些高阶抽象和物理模型。比方说做个傅立叶变换，这是纯数学的，用Numpy；做个滤波器，这属于信号处理模型了，在Scipy里找。
- Pandas提供了一套名为DataFrame的数据结
构，比较契合统计分析中的表结构，并且提供了计算接口，可用Numpy或其它方式进行计算

### pandas 基本用法→处理数据

- 读取csv文件, names表示列标签，可以忽略

      import pandas as pd
      test_pd = pd.read_csv('xxx.txt', names=["a", "b", "c"])

- 排序

      test_pd.sort.sort_values(by="a")
      # test_pd.sort.sort_values(by=["a","b"])
- 删除行

      test_pd[test_pd[(test_pd["a"]>0) & (test_pd["b"]>0)]]
      test_pd.drop_duplicates("a")#删除a列重复的值


- 写入csv或者txt文件

      test_pd.to_csv("xx.csv", header=None,index=None)
      # header 表示列名， index 表示行名
