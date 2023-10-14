---
layout: post
title: "Kelly Criterion"
date: 2022-11-24
---

#### **凯利公式**

$$
f^{*} = p - \frac{q}{b}
$$

其中：

- $$p$$ 为胜率
- $$b$$ 为赔率（不含本金）
- $$f^{*}$$ 为最优投注比例
- $$q = 1 - p$$ 为输率
- $$f$$ 为最优投注比例

#### **推导过程**

成功后的资金为 $$1 + bf$$

失败后的资金为 $$1 - f$$

所以资金的几何增长率为：

$$
r = (1 + bf)^p \cdot (1 - f)^q
$$

对其取对数后得到：

$$
E = \ln r = p \cdot \ln (1 + bf) + q \cdot \ln (1 - f)
$$

对 $$E$$ 求导：

$$
\frac{\partial E}{\partial f} = \frac{bp}{1 + bf} - \frac{q}{1 - f} = 0
$$

解得：

$$
f^{*} = \frac{bp - q}{bp + bq} = p - \frac{q}{b}
$$


#### **参考资料**

1. <https://en.wikipedia.org/wiki/Kelly_criterion>
