---
layout: post
title: “Pattern generation on rough surface”
subtitle: Solving PDEs on rough surface
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


## Thoughts
Rough surfaces with larger M&N
- Sure

Effects of different diffusion tensors
-  But how exactly? 只知道大对应大小对应小
- （btw，如果reverse max and min的话，会得到恰好相反的hill和valley

PDE setup for real life patterns
- 可是roughness有啥用？
- 模拟动物特定部位？
- 更细小的roughness制造图形在皮肤上的不规则？（这个不错！）可是应该如何衡量这个roughness？一张张改吗有什么价值？每只动物的roughness都不一样啊

![Animal skin pattern](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRkW8wtwJ6rjXTuaX3uTNnc1zdBds_pNC-UVQ&usqp=CAU)

所以其实r-d model模拟动物表皮生成这个事情还没有被完全证实。目前是在鱼类上有实例，所以替代方案都有什么？

## 需要的论文领域
几种可能的纹路对象，reaction-diffusion equation，参数和模型
- 动物表皮 （重点看生成，微结构对纹路的影响）
[Reaction Diffusion Equations and Animal Coat Patterns](https://www.sjsu.edu/faculty/watkins/murray.htm)
- 地质，石纹路形成
- 沙丘形成
- 气流模拟


## 手里的论文
- 关于介绍multi-component RD systems，通过简单的两chemicals r-d model推论而来