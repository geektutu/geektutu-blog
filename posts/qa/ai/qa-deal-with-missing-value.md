---
title: 机器学习面试题-如何处理特征向量的缺失值
date: 2018-07-03 10:51:24
description: 机器学习面试题系列文章，如何处理特征向量的缺失值
tags:
- 机器学习
- 面试题
catagories:
- 机器学习
---

> - **持续整理有温度、有难度、有热度的机器学习面试笔试题。**
> - [机器学习面试笔试题 - Github](https://github.com/geekcircle/machine-learning-interview-qa/)
> - [机器学习面试笔试题 - Gitbook](https://geekcircle.org/machine-learning-interview-qa/)

## 1) 缺失值较多

缺失值较多.直接将该特征舍弃掉，否则可能反倒会带入较大的噪声，对结果造成不良影响。

## 2) 缺失值较少

缺失值较少，其余的特征缺失值都在10%以内，我们可以采取很多的方式来处理:

- 方式1: 把NaN直接作为一个特征，假设用0表示；

    ```python
    data_train.fillna(0)
    ```
- 方式2: 用均值填充；

    > 均值填充可能需要取条件均值，例如某训练集中患癌症和不患癌症的数据中，该值的差距很大，那么就应当填充label相同的数据的均值。

    ```python
    data_train.fillna(data_train.mean())
    ```

- 方式3：用上下数据进行填充；

    ```python
    # 上一个数据填充
    data_train.fillna(method='pad')
    # 下一个数据填充
    data_train.fillna(method='bfill')
    ```

- 方式4：插值法

    ```python
    # 即估计中间点的值
    data_train.interpolate()
    ```
- 方式5：用随机森林等算法拟合

    > 将数据分为有值和缺失值2份，对有值的数据采用随机森林拟合，然后对有缺失值的数据进行预测，用预测的值来填充。