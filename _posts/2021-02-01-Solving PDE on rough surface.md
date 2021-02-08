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
-** ！动物表面有一些disorder，可以用这个模拟！**

![Animal skin pattern](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRkW8wtwJ6rjXTuaX3uTNnc1zdBds_pNC-UVQ&usqp=CAU)

所以其实r-d model模拟动物表皮生成这个事情还没有被完全证实。目前是在鱼类上有实例，所以替代方案都有什么？

> In addition to reaction-diffusion, other mathematicalmodels (Murray, 1989; Maini et al., 1991) have beenproposed to explain biological pattern formation, for examplethe chemotactic model and the neural net model.

## 需要的论文领域
讲一下历史，首先要证明reaction-diffusion equation的可行性
- 已知在鱼身上有，zebrafish常用，目前找到的论文都比较早期，找一下更近的


几种可能的纹路对象，reaction-diffusion equation，参数和模型
- 动物表皮 （重点看生成，微结构对纹路的影响）
[Reaction Diffusion Equations and Animal Coat Patterns](https://www.sjsu.edu/faculty/watkins/murray.htm)
- 地质，石纹路形成
- 沙丘形成
- 气流模拟
- 声波驱动的纹理


## 手里的论文
- 比较近期的论文。关于介绍multi-component RD systems，通过简单的两chemicals r-d model推论而来。Do not require differential diffusivity, challenged classical view of local self-activation and lateral inhibition.

- 动物皮肤pattern生成与皮下组织无关，因此没有prepattern。具体是怎样？不太理解。前几年r-d model一直不太被认可，但是有在fish skin发现对应的pattern。需要注意的是，这篇论文发表于2002年。

- zebrafish的一篇提出，随着stripe的生长，增大空间大小，因为鱼在生长。我有必要这样做吗？


## Diffusion tensor & operator

- Adjugate Diffusion Tensors for Geodesic Tractography in WhiteMatter
传统方法：inverse diffusion tensor
此处方法：adjugate metric

high angular resolution diffusion imaging (HARDI)普遍比 diffusion tensor imaging（DTI）要好，但是DTI还在被应用着。因为HARDI时间用的比较长，而且not available。
两种对于标准方法的主要modification：

1. "sharpening" 可以制造更好的tractography results，但是弊端是robustness to noise会下降，所使用的parameter是chosen in ad hoc way （？）
  - $D_{sharp}=D^n$, D是diffusion， $D_{sharp}$是sharpened tensor， n>1. 
  - “Fiber” tensor：同时，Descoteaux et al. 有不同的sharpening strategy，依赖于diffusion tensor的transformation。（Descoteaux, M., Deriche, R., Lenglet, C.: Diffusion tensor sharpening improveswhite matter tractography. In: SPIE Image Processing: Medical Imaging, pp. 1084–1087. San Diego (2007)）
2.  “based on conformal rescaling of standard Riemannian metric"
$g_{Hao}=e^{\alpha}D^{-1}$, 在这里$\alpha$是通过requiring geodesiccurves to follow more closely the diffusion tensor principaleigenvectors得到的。文章中提到的方法和这种方法比较类似。
（Hao, X.,Whitaker, R.T., Fletcher, P.T.: Adaptive Riemannian metrics for improved geodesic tracking ofwhite matter. In: Székely, G.,Hahn, H.K. (eds.) IPMI 2011. Lecture Notes in Computer Science, vol. 6801, pp. 13–24. Springer, Berlin (2011)）
