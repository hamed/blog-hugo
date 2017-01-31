+++
tags = []
draft = false
date = "2016-12-27T11:20:18+03:30"
title = "Potty training and survival analysis"
description = "Hardcore math and parenting"
categories = ["data-science", "parenting"]

+++

It is time to potty train the Little One (LO). 
The objective is to use Reinforcement Learning (RL) so the LO pisses in the toilet instead of his diaper. 
The idea of RL is to keep LO on his potty until he accidentally pisses into that. 
Then mommy and daddy are ecstatic, jumping up and down with enormous joy, 
giving him lots of kisses, stickers and chocolates. 
We need to repeat the process over and over again to reinforce the good behavior into the little cute tiny brain of LO. 
It is simple but it is not easy. 
Survival analysis might come handy. 
<!--more-->

During the training, LO pisses on different parts and objects of the house, 
from mom’s favorite carpet to dad’s smart phone (False Negatives). 
If we want to avoid that, 
we have to wait endless hours in the bathroom until the LO gets fed up leaves with no result (False Positives).

So, the objective is to minimize false positives and false negatives, 
spend less time in the toilet, and spend less time cleaning the house.

Let P(t) be the probability of LO pissing during t and t+dt. 
This is not a uniform Probability Density Function (PDF). 
It depends on many parameters, like room temperature, water consumption and  sweating. 
It is even more complicated that that, P(t) depends on the history, 
it depends on what happened at before, the last time LO has pissed. 
Maybe we can use some survival analysis here.

In survival analysis, we are interested in calculation of survival function S(t), 
the probability of LO keeping all the urine in his tiny bladder as long as t, 
given that he has already pissed at time t=0. 
So for example, in our case study we are confident that S(15 min) = 1 and S(4 hour)=0, 
for awake subject but for asleep subject, S(t) stays close one for as long as 12 hours.

For awake subject, the half life is about 2 hours, 
half of the time he can keep his pajama dry as long as two hours.

After a series of observations, we come to this conclusion:

**First thing in the morning, put LO on his potty. In a couple of minutes, LO will fill both the potty and your cup of joy!**

**Then, you are almost safe during next hour, at the end of first one hour, you give it a shot, then you will try half an hour later and a quarter later and then you leave LO on the potty until he pisses.**

Have a good potty training! But be aware that the parameters of your LO might be different from ours!

*Originaly published on my [Linkedin](https://www.linkedin.com/pulse/potty-training-data-scientists-way-hamed-seyed-allaei) page.* 

