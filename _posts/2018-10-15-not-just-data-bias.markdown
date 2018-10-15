---
title: "Algorithmic Bias is Not Data Bias"
layout: post
date: 2018-10-15 12:19
image: /assets/images/markdown.jpg
headerImage: false
tag:
- bias
- machine-learning
star: false
category: blog
author: aaronspringer
description: 
---
This myth is perpetuated across message boards to research articles and everything in between. It is so widespread that I simply have to say something about it. _Algorithmic bias is not just data bias_. Sure, “data bias” may be a root cause in many algorithmic bias problems and researchers should always be well aware of the sampling characteristics of their training sets. However, algorithmic bias is not simply a problem where the algorithm was trained on a dataset that was missing information or unrepresentative of a larger population, it can be much more pernicious that that.

Word embeddings illustrate that ‘algorithmic bias is not just data bias’. Word embeddings embody biases that are implicit in the way we talk about people. [When looking at word embeddings, the professions most associated with ‘she’ contain ‘homemaker’, ‘nurse’, ‘receptionist’](http://papers.nips.cc/paper/6227-man-is-to-computer-programmer-as-woman-is-to-homemaker-debiasing-word-embeddings). Most associated with ‘he’ are words like ‘captain’, ‘magician’, and ‘boss’. Is this an issue of data bias? No. Even if these word embeddings were trained on every single written English word that exists we would get the same outcome. These words reflect our society well. However, building upon these word embeddings could result in biases that disadvantage women using them. [Advertising higher paying jobs exclusively to men comes to mind](https://www.theguardian.com/technology/2015/jul/08/women-less-likely-ads-high-paid-jobs-google-study).

This is just a single example illustrating the fact that algorithmic bias is not just data bias. Unfortunately, asserting this fact opens up an algorithmic Pandora’s Box. If algorithmic bias is always just data bias, then we can correct it by collecting more data or reweighting our sample. Unfortunately, it is not that simple. We are arriving at a world where these problems cannot be fixed by technical considerations; these problems must be fixed by ethical considerations.

