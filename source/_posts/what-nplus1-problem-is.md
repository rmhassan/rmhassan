---
extends: _layouts.post
section: content
title: What N+1 problem actually is?
date: 2021-04-03
categories: [algorithm, n+1, coding]
featured: true
description: Do you have big data to work with? Do you retrieve data that is related to other data(which most of the time is)? You may be facing N+1 problem. But do you know what N+1 problem is?
---

I was reading a [post](https://laravel-news.com/18-tips-to-optimize-your-laravel-database-queries) on Laravel news which includes a number of tips to improve your database queries. It has tons of stuff that everyone should be aware of. Tip#5 specifies that you should be aware of N+1 problem. It explains clearly what the N+1 problem is.

> So if there are N number of posts, it will make N+1 queries( 1 query to retrieve posts and N queries to retrieve the author for each post). This is commonly known as N+1 query problem.

What does this essentialy means that if you have 10 posts, and you do 1 query to retrieve that 10 posts. But there are actually 11 queries running. 1 to get 10 posts and other 10 to retreive authors of these 10 posts.

This is commonly know as N+1 problem.
