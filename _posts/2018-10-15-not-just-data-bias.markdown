---
title: "Algorithmic Bias is Not Just Data Bias"
layout: post
date: 2018-10-15 12:19
image: /assets/images/markdown.jpg
headerImage: false
tag:
- bias
- machine-learning
- fairness
star: false
category: blog
author: aaronspringer
description: 
---
This myth is perpetuated across message boards to research articles and everything in between. It is so widespread that I simply have to say something about it. _Algorithmic bias is not just data bias_. Sure, “data bias” may be a root cause in many algorithmic bias problems and researchers should always be well aware of the sampling characteristics of their training sets. However, algorithmic bias is not simply a problem where the algorithm was trained on a dataset that was missing information or unrepresentative of a larger population, it can be much more pernicious that that.

The first example is one you’re likely familiar with: COMPAS. COMPAS is a system some governments use to determine parole and sentencing in judicial settings. [ProPublica wrote an article about this system and how it was biased against people of color](https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing). It is impossible to know the details given the proprietary formula used for COMPAS, but it is easy to speculate that COMPAS was trained using data from the current judicial system.[Given that our current judicial system produces harsher punishments for defendents of color](https://link.springer.com/content/pdf/10.1023/A:1015258732676.pdf) then it is no wonder COMPAS is biased. Isn’t this a result of a biased dataset? Not really, this data could be perfectly representative of the population it was drawn from. Even if we had all data from every parole decision ever made, we would likely get the same outcome. Our dataset is not statistically biased from the overall population. Rather, what we see in this type of data is a bias or difference from some hypothesized 'ideal' dataset where folks are treated fairly by our judicial system.

Word embeddings illustrate that ‘algorithmic bias is not just data bias’ as well. Word embeddings embody biases that are implicit in the way we talk about people. [When looking at word embeddings, the professions most associated with ‘she’ contain ‘homemaker’, ‘nurse’, ‘receptionist’](http://papers.nips.cc/paper/6227-man-is-to-computer-programmer-as-woman-is-to-homemaker-debiasing-word-embeddings). Most associated with ‘he’ are words like ‘captain’, ‘magician’, and ‘boss’. Is this an issue of data bias? No. Even if these word embeddings were trained on every single written English word that exists we would likely get the same outcome. These words reflect our society well. However, building upon these word embeddings could result in biases that disadvantage women using them. [Advertising higher paying jobs exclusively to men comes to mind](https://www.theguardian.com/technology/2015/jul/08/women-less-likely-ads-high-paid-jobs-google-study).

The above are just a couple examples illustrating the fact that algorithmic bias is not just data bias. Unfortunately, asserting this fact opens up an algorithmic Pandora’s Box. If algorithmic bias is always just data bias, then we can correct it by collecting more data or reweighting our sample. Unfortunately, it is not that simple. To correct these problems requires counterfactual thinking. Correcting these problems requires articulating a clear vision for what constitutes fair treatment and using newly developed techniques to enforce this when training a model. We are arriving at a world where fairness and algorithmic bias problems cannot be fixed by technical considerations; these problems must be fixed by ethical considerations.
