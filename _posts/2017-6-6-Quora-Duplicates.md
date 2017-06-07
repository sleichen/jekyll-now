---
layout: post
title: Quora Question Pairs
published: false
---

Today the Kaggle competition Quora Question Pairs finished. The point of this competition was to figure out if pairs of questions had the same meaning. Of course this has the potential to become very complicated. In fact, in reading the Kaggle discussion boards it became clear that others in the competition were implementing *very* complicated models. For me, right now, these competitions are a learning experienceso my model was very basic. In this post I'm going to describe what I did for this competition. Note that I gathered many of the ideas from reading the Kaggle dsicussion forums, but that's the best way to get started in this stuff.

This competition was a binary classification problem. We were given a large set of question pairs that were labeled as either duplicates or not as the training set, and had to predict the probability that each pair of a separate set were duplicates.