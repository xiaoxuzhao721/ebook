# 利用Python进行数据分析第二版
## 常用模块的命名惯例
```
import numpy as np

import matplotlib.pyplot as plt

import pandas as pd

import seaborn as sns

import statsmodels as sm

import bisect #bisect.bisect 可以找到插入值后仍保证排序的位置，bisect.insort是向这个位置插入值
```
## python 知识点总结

- 三元表达式：value = true-expr if condition else false-expr
- 列表推导式：[expr for val in collection if condition]
- .count 统计某个值的出现频率，适用于列表跟元组
- .insert(index,value) 可以在特定的位置插入元素
- .pop(index) 移除并返回指定位置的元素，如果集合为空，会抛出KeyError错误
- .remove(value) 会寻找第一个值并除去
- .extend(value) 可以追加多个元素
- .sort() 将一个列表原地排序
- enumerate函数，返回（i,value）元组序列
- sorted函数：可以从任意序列的元素返回一个新的排好序的列表
- zip函数：将多个列表、元组或者其他序列对组合成一个元组列表
- reversed :从后向前迭代一个序列
