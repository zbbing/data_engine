# -*- coding: utf-8 -*-
"""
Created on Sun Jun 14 22:10:54 2020

@author: ZhangBaibing
"""


# 作业1
import numpy as np
data= np.arange(2,101,2)
print(data.sum())

#作业2
from pandas import DataFrame

data = {'Chinese':[68,95,98,90,80],'Math':[65,76,86,88,90],'English':[30,98,88,77,90]}

df = DataFrame(data,index=['ZhangFei','GuanYu','LiuBei','DianWei','XuChu'])
print(df.describe())
print(df.var())
print(df.std())
df['总分']=df.sum(axis=1)
print(df.sort_values(by='总分', ascending=False))

#作业3
import pandas as pd

result = pd.read_csv('car_complain.csv')
result = result.drop('problem',1).join(result.problem.str.get_dummies(','))
df = result.groupby(['brand'])['id'].agg(['count'])
print('品牌投诉总数：',df.sort_values('count',ascending=False))
df1 = result.groupby(['car_model'])['id'].agg(['count'])
print('品牌投诉总数：',df1.sort_values('count',ascending=False))
df2 = result.groupby(['brand','car_model'])['id'].agg(['count'])
print('品牌投诉总数：',df2.sort_values('count',ascending=False))
