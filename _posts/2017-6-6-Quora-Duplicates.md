---
layout: post
title: Quora Question Pairs
published: false
---

Today the [Kaggle](https://www.kaggle.com/) competition [Quora Question Pairs](https://www.kaggle.com/c/quora-question-pairs) finished. The point of this competition was to figure out if pairs of questions had the same meaning. Of course this has the potential to become very complicated. In fact, in reading the Kaggle discussion boards it became clear that others in the competition were implementing _very_ complicated models. For me, right now, these competitions are a learning experience so my model was very basic. In this post I'm going to describe what I did for this competition. Note that I gathered many of the ideas from reading the Kaggle discussion forums, but that's the best way to get started in this stuff.

This competition was a binary classification problem. We were given a large set of question pairs that were labeled as either duplicates or not as the training set, and had to predict the probability that each pair of a separate set were duplicates. All of these classification problems have two main parts:

1. Feature Engineering
2. Model Selection and Training

In the rest of this post I'll explain what I did for each of these, and a little about what I would do differently with more time and/or computing resources

## Feature Engineering ##

Probably the most important part of building a classifier is the Feature Engineering. A Feature is some aspect of the data that you use as input for the model. In this case, simple features would be things like the number of words in each question of a pair, or the number of words that the two questions have in common. I used a few simple features like that, but also a couple of more complicated ones created using something called Word2Vec.

Word2Vec.....

In then end I think most of my success came from the simple "how many words do the questions have in common" feature. I would definitely spend a lot more time and effort on feature engineering in the future. I read on the forms that some people had hundreds of features in their models! Unfortunately, I don't have the computing power for that sort of thing, so the number of features I could use is inherently limited.



## Model Selection and Training ##

It's important for me at this early stage to do something new with each project. This time the big new thing was [XGBoost](http://xgboost.readthedocs.io/en/latest/), which is a very modern tool implementing boosted decision trees. I'm not super familiar with the technical details yet (that will come), but it seems to work really well. Part of the beauty of packages like XGBoost is that you don't really need to know the technical ins-and-outs of it to put it to use. So all I really had to do was install it and follow some tutorials to run it. Installing these things is always easier said than done for me, but this time I was able to do it without too much trouble.



## Final thoughts ##

Overall I feel like I learned a lot from participating in this competition. XGBoost seems like a really important tool for my toolbox, and I'm surely going to use it a lot more in the future. Someday (soon?) I'll have to start using some sort of cloud computing solution to do more complicated models like the pros, but for now I can get away with my little ol' laptop. If you're interested in seeing the code I wrote, you can check it out in my [GitHub repository](https://github.com/sleichen/Quora-Question-Pairs).
