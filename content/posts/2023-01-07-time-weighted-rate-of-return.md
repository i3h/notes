---
layout: post
title: "Time-Weighted Rate of Return"
date: 2023-01-07
---

#### **概述**

时间加权回报（TWR）是一种计算投资回报的方法，它可以消除资金进出带来的回报率计算扭曲。

TWR 根据资金变动，计算各个时间子区间的回报率，最后相乘得到几何平均回报率。

#### **公式**

无资金变动时的回报率：

$$
R = \frac{M_2-M_1}{M_1}
$$

- $$M_1$$ 为初值
- $$M_2$$ 为终值
- $$R$$ 为回报率

增长因子为：

$$
1+R = \frac{M_2}{M_1} 
$$

假设在周期开始时有资金变动$$C_1$$，对初值$$M_1$$进行补偿：

$$
R = \frac{M_2-(M_1+C_1)}{M_1+C_1}\\
~\\
1+R = \frac{M_2}{M_1+C_1}
$$

最后将所有子区间的回报率相乘可得：

$$
1+R=\frac{M_1}{M_0+C_0}\times\frac{M_2}{M_1+C_1}\times\frac{M_3}{M_2+C_2}\times...\times\frac{M_{n-1}}{M_{n-2}+C_{n-2}}\times\frac{M_{n}}{M_{n-1}+C_{n-1}}=\prod_{i=0}^{n-1}\frac{M_{i+1}}{M_{i}+C_{i}}
$$

#### **参考资料**

1. <https://en.wikipedia.org/wiki/Time-weighted_return>
2. <https://www.investopedia.com/terms/t/time-weightedror.asp>
