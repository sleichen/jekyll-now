---
layout: post
title: Big Query
published: true
---

This post is about Google's [Big Query](https://cloud.google.com/bigquery), which had _planned_ to use for a project in the near future (more on that below). Big Query is cloud database run by Google that you can store your data in for a fee and access it later. There are also lots of publicly-available databases on Big Query, which one could take advantage of. And there are not-officially-public-but-still-publicly-accessible databases too. For instance, every Reddit post ends up there. I assume that's due to the generosity of some person who likes data and doesn't mind paying fees. The people at Google have figured out how to make searching the databases extremely fast, even when they're very large. [Here](https://www.youtube.com/watch?v=UueWySREWvk) is a really interesting video about it.

Accessing data on Big Query is done through a SQL-like language. Since I'm not a SQL expert yet, I figured that using Big Query for a side project would be a good way to learn SQL hands-on. So I say down the other day and started querying the NYC taxi public database (which has an entry for every taxi ride in NYC!). I didn't have any particular goal in mind, I was just writing some random queries. For each one, Big Query will tell you how many GB of data it's going to sift through to return the answer. Many of the queries I was writing were requring ~100GB of data. And it turns out that Big Query only lets you access 1TB of data per month before you have to start paying... Welp, it didn't take much before I received a message telling me I'd used up my whole quota! So much for that. I guess I'll have to learn SQL some other way.
