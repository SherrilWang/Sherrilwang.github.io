---
layout: post
title: “Pattern generation on rough surface （二）”
subtitle: 关于parameter的调整：M，f, D｜和leevan的探讨

author: "Sherril"
header-img: "img/sky.jpeg"


header-mask: 0.3
tags:

 - Mathematics
---

一些关于论文的想法。
批注颜色：
- 红色：非常非常重要
- 橘色：理论陈述
- 黄色：次重要理论
- 蓝色：存疑
- 绿色：数据分析 


# What to adjust
## M: Surface Complexity
通过提高M调整粗糙程度，具体多大？需要实验

## D： Diffusion Tensor
[Diffusion Tensor](http://mriquestions.com/diffusion-tensor.html)
不同的D (或者说operator)有着不同的结果： 具体怎么影响？
- Adjugate diffusion tensor


## f
暂时没什么想法。

## 各个参数的调整
取某个特定数值？取range内变化？


# 下一步咋整
经过和leevan的探讨，尝试逐步调整M，N，并观察pattern随之变化的情况。Amplitude的大小也可以调整一下并作观察。

一个小发现：一些journal允许你上传fig file，比如Engineering Analysis with Boundary Elements.

读一下这几篇论文，是Steven写的
[Extrinsic Meshless Collocation Methods for PDEs on Manifolds](https://epubs.siam.org/doi/10.1137/17M1158641)

[Implicit-Explicit Methods for Time-Dependent Partial Differential Equations](https://epubs.siam.org/doi/abs/10.1137/0732037?mobileUi=0)

[A simple embedding method for solving partial differential equations on surfaces](https://dl.acm.org/doi/abs/10.1016/j.jcp.2007.10.009)

接下来要研究意下如何把rough surface从平面到立体图形上，是否可以通过eigenvector直接建立平面？那就要考虑到连续性的问题。（算一下试试看）

