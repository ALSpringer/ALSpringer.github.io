---
title: "Learning by Doing: Logistic Mixed Models"
layout: post
date: 2021-05-23 12:19
image: /assets/images/markdown.jpg
headerImage: false
tag:
star: false
category: blog
author: aaronspringer
description:  
---
I'm in a weird stage right now. I use a lot of complex statistics at work regularly, but I've learned most of them through pragmatic means and without a lot of formal education. I am quite careful that I do my due diligence on assumptions, model checking, and such but I'm dissatisfied with my root understanding on how some of these models work. Specifically I'm thinking about some of the generalized linear mixed models I've been using recently. I often have questions that I need to look up that I should perhaps know the answer from first principles if I understood the underlying estimation procedure better.

 I've become a lot more knowledgeable about mixed-models recently, but I've also realized how little I really know. I'm also dissatisfied with the state of doing this type of modeling in Python; statsmodels is a fantastic package but the support for generalized linear mixed models feels sparse compared to R's fantastic glmer package.

I'm setting out to code a logistic mixed-model from scratch in order to better understand how these models are estimated. Maybe one day I'll be able to contribute back to statsmodels but I'm afraid those folks are much smarter than I am when it comes to stats packages.

I see a natural progression here that I'm hoping to follow:
1. Create a function for estimating basic multiple linear regression models
2. Create a function for estimating linear mixed models
3. Create a function for estimating logistic mixed models

To be honest, I don't know what I don't know. This could take much longer than I'm expecting. And I do believe there is a bit of a disconnect between points 1 and 2. I think I'll have to move from being able to directly calculate the model to an iterative estimation process but I'd like to get a small win first with the multiple regression before moving on.

I want to set out some requirements for the first multiple regression stage so I can hold myself to them:
1. The regression function should produce coefficient estimates nearly identical to lm() in R
2. The function should also produce 95% confidence intervals for the coefficient estimates. I'd like to estimate these via bootstrapping but we will see.
3. The regression function should also produce an overall p-value for the model.
4. "From scratch" here is a bit ill-defined but I intend to write this at the level of calling the matrix operations from a package like numpy but not writing my own matrix inversion function or the like.

I'll provide updates on the process as I go.
