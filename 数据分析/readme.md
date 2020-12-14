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
- .count 统计某个值的出现频率，适用于列表跟元组
- .insert(index,value) 可以在特定的位置插入元素
- .pop(index) 移除并返回指定位置的元素
