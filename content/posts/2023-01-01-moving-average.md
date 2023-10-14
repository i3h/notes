---
layout: post
title: "Moving Average"
date: 2023-01-01
---

#### MA (Moving Average)

移动平均是计算时间序列数据中某个子集的平均值的方法。在金融领域，移动平均是一种常用的技术分析工具，用于分析股票价格、货币汇率、利率等。移动平均的计算方法有很多种，最常用的是简单移动平均和加权移动平均。

#### SMA (Simple Moving Average)

简单移动平均是未加权的计算方式，比如有一个时间序列 [5, 6, 7, 8, 9]，计算周期为 3 的简单平均如下：

第一天：(5 + 6 + 7) / 3 = 6

第二天：(6 + 7 + 8) / 3 = 7

第三天：(7 + 8 + 9) / 3 = 8

#### WMA (Weighted Moving Average)

加权移动平均会给每个序列值赋予权重后再计算平均，时间上越近，权重越高。

比如要计算周期为 5 的移动平均，则可以给最近的 5 个数值赋予权重分别为：5, 4, 3, 2, 1

计算公式为：

$$
\frac{\sum value \times weight}{n}
$$

#### EMA (Exponential Moving Average)

指数移动平均是加权移动平均的一种计算方法，它以指数衰减的方式赋予时间序列权重。时间序列中的每个值都会一直参与计算而不会被剔除，但越远的数据获得的权重会急剧降低。

EMA 的计算过程分为 3 步：

1. 计算 SMA：

    $$
    SMA = \frac{\sum value}{n}
    $$

2. 计算乘数：

    $$
    multiplier = \frac{2}{n + 1}
    $$

3. 计算 EMA：

    $$
    EMA(t) = (x(t) - EMA(t-1)) \times multiplier + EMA(t-1)
    $$

- 当 $$t = 1$$ 时，使用 $$SMA(0)$$ 替代 $$EMA(0)$$
- $$x(t)$$ 为当前的时间序列值

这里用到了指数平滑公式：

$$
s_t = \alpha x_t + (1 - \alpha)s_{t-1} = s_{t-1} + \alpha (x_t - s_{t-1}), \:\alpha \in [0, 1]
$$

- $$\alpha$$ 为平滑因子

#### **参考资料**

1. <https://www.tradingview.com/support/solutions/43000502589-moving-average/>
2. <https://en.wikipedia.org/wiki/Moving_average>
3. <https://en.wikipedia.org/wiki/Exponential_smoothing>