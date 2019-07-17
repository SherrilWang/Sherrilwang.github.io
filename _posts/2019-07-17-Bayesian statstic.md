---
layout: post
title: “对于Bayesian Statistics的初步认识"
subtitle: '和Frequentist stat的比较/主要方法和思路/未完'
author: "Sherril"
header-img: "img/google-earth-view-5553.jpg"

header-mask: 0.3
tags:
  - Bayesian Statistics
  - Mathematics
  - notes
---



 ![图片描述-w300](https://i.loli.net/2019/07/17/5d2e9dbb3623d34138.jpg)

# Frequentist Statistics 

- Frequentist Statistics tests whether an event (hypothesis) occurs or not. It calculates the probability of an event **in the long run** of the experiment (i.e the experiment is repeated under the same conditions to obtain the outcome).

## Common flaws
- 结果准确度对实验重复次数的依赖性
- 依据固定样本量的sample stat计算的 p-values 会依stopping intention和sample size而变化。
- Confidence Interval (C.I) 同样高度依赖于样本量的大小。
- Confidence Intervals (C.I) are not probability distributions therefore they do not provide the most probable value for a parameter and the most probable values. （？）


# Bayesian Statistics
- Bayesian statistics is a theory in the field of statistics based on the Bayesian interpretation of probability where probability expresses a **degree of belief** in an event

一种根据前面出现的结果不断更新概率的统计过程，。

## Bayes Theorem
![图片描述-w300](https://i.loli.net/2019/07/17/5d2e986f7d7db82219.jpg)

## Bayesian inference
*Models* 
- the mathematical formulation of the observed events. 

*Parameters*
- are the factors in the models affecting the observed data. 

## Bernoulli likelihood function
![](https://i.loli.net/2019/07/17/5d2e99a65289d89320.jpg)
其在Bayesian stat里的意义是

## Prior Belief  Distribution
### beta distribution
![](https://i.loli.net/2019/07/17/5d2e99f42580f30096.jpg)
 
 In a toss game, $\alpha$ and $\beta$ can be taken as the outcomes of head and tail.

## Posterior Belief Distribution
通过Prior 和 likelihood 得到 Posterior。

![](https://i.loli.net/2019/07/17/5d2e9df587d6a44359.jpg)


![](https://i.loli.net/2019/07/17/5d2e9be33829356870.jpg)
 ![](https://i.loli.net/2019/07/17/5d2e9bc8403a649028.jpg)
 ![](https://i.loli.net/2019/07/17/5d2e9bf274a5d36991.jpg)

Get: 
![](https://i.loli.net/2019/07/17/5d2e9bd30eb7252170.jpg)


## Bayes Factor

"Bayes factor is the equivalent of p-value in the bayesian framework. "
![图片描述-w300](https://i.loli.net/2019/07/17/5d2e9c83cfeca70926.jpg)

## High Density Interval
"HDI is formed from the posterior distribution after observing the new data."
- independent of intentions and sample size

![图片描述-w300](https://i.loli.net/2019/07/17/5d2e9d00d504721202.jpg)



# Refrence
https://www.analyticsvidhya.com/blog/2016/06/bayesian-statistics-beginners-simple-english/

https://towardsdatascience.com/bayesian-statistics-for-data-science-45397ec79c94?gi=4be4fe59bb5f


