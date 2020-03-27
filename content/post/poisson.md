---
title: ポアソン分布
author: ~
date: '2020-03-27'
slug: prob
categories: [統計]
tags: []
Categories:
Description: ''
Tags:
menu: ''
---

# ポアソン分布
ある一定の時間や空間において、平均でλ回発生する事象がｘ回発生する確率。地震発生確率、サッカーの得点確率、保険料の算出、食中毒の件数予測等
$$
f(x) = \frac{e^{-\lambda}\lambda^x}{x!}
$$

期待値　$E(X)=λ$  
分散　　$V(X)=λ$  



```python
import numpy as np
import matplotlib.pyplot as plt
from scipy import stats
from scipy.stats import poisson

x =  np.arange(1, 100, 1)
y1= [poisson.pmf(i, 10) for i in x]
y2= [poisson.pmf(i, 20) for i in x]
y3= [poisson.pmf(i, 30) for i in x]
y5= [poisson.pmf(i, 50) for i in x]
y10= [poisson.pmf(i, 100) for i in x]

plt.bar(x, y1, align="center", width=0.4, color="red"
                ,alpha=0.5, label="Poisson λ= %d" % 10)

plt.bar(x, y2, align="center", width=0.4, color="green"
                ,alpha=0.5, label="Poisson λ= %d" % 20)

plt.bar(x, y3, align="center", width=0.4, color="blue"
                ,alpha=0.5, label="Poisson λ= %d" % 30)

plt.bar(x, y5, align="center", width=0.4, color="orange"
                ,alpha=0.5, label="Poisson λ= %d" % 50)

plt.bar(x, y10, align="center", width=0.4, color="Cyan"
                ,alpha=0.5, label="Poisson λ= %d" % 100)

plt.legend()
plt.show()
```


![png](poisson_files/poisson_1_0.png)



