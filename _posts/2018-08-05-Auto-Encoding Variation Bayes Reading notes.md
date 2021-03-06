---
layout: post
title: 'Auto-Encoding Variational Bayes Reading Notes'
date: 2018-08-05
author: naykun
cover: 'https://cdn-images-1.medium.com/max/1600/0*OW0FnEOMhIDxpPv5.jpg'
tags: Deeplearning
---

# Auto-Encoding Variational Bayes

# 简要翻译

## 摘要

面对有着棘手的后验分布的连续隐变量和巨大的数据集，我们如何能有效地使用有向概率模型进行学习和推断？我们提出了一种随机变分的推断和学习方法来适应大数据集，甚至在某些温和的可微分条件下，对某些不可解问题仍然奏效。我们的贡献主要有两个部分。首先，我们展现了变分下界的再参数化可以构建一个下界评估器，可以直接使用标准的随机梯度下降方法进行优化。第二，我们发现对于每个数据点都有连续隐变量的独立同分布数据集，通过使用下界评估器在不可解后验条件上拟合一个近似的识别模型来进行后验推断变得十分有效。理论的正确性在实验结果上得到了验证。

## 1 引言

