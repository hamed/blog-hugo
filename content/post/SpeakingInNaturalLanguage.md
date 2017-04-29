+++
draft = true
description = ""
date = "2017-04-29T15:11:49+04:30"
title = "Speaking In Natural Language"
categories = []
tags = []

+++

# Me and NLP
For a long time I wanted to learn Natural Language Processing, but I didn't have the time. 
Now that there is a competition on Kaggle [Quora Question Pairs](https://www.kaggle.com/c/quora-question-pairs), 
I want to seize the opportunity and learn it hands on. 
While learning and practicing, I document everything here for others and for my future me!
<!--more-->

# Duplicate or no?
The goal is to predict if a pair of questions are duplicate or not. 
The training set provides 404290 labeled question pairs (1, they are duplicate, 0, they are not duplicate). 
We have to predict the probability of being duplicate for any new pair of questions. 

# The most naive solution
It is easy to get lost in the complexity of a model,
so as a benchmark and an starting point,  
I use the simplest model of all 
and I guess the probability of duplicates only from the frequency of duplicates in the training set.
The code is [here](https://www.kaggle.com/pinocchio/quora-question-pairs/naive/run/1116931).

Its log loss is 0.55411, and it ranks 1727 out of 2168, it exceeds my expectations!
The best solution as of this writing is 0.12684 so I have a long way to go. 

