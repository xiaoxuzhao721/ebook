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
## 数据清洗和准备
- 滤除缺失数据
1. dropna  

df.dropna()丢弃任何含有缺失值的行
df.dropna(how='all')丢弃全为NA的那些行
df.dropna(axis = 1,how = 'all')丢弃全为NA的那些列
df.dropna(thresh =n)保留至少有n个非NaN数据的行/列
2. isnull/notnull

df\[df.notnull()]
- 填充缺失数据
1. fillna
df.fillna(n)全部缺失值用常数n填充
df.fillna({列名1：value1,列名2：value2})根据列名填充不同的值
df.fillna(df.mean())填充平均值或者中位数
- 移除重复数据
df.duplicated()
df.drop_duplicates()重复的数组会标为False
df.drop_duplicates([列名])根据某一列过滤重复项
df.drop_duplicates(\[列名1，列名2],keep='last')默认保留第一个出现的组合，传入keep='last'则保留最后一个
- 数据转换
map方法，可以接受一个函数或者含有映射关系的字典
- 数据替换
replace方法
- 重命名索引轴
rename方法
- 离散化
pd.cut()
## 正则表达式
