---
extends: _layouts.post
section: content
title: Laravel 8 - Retrieve one or two columns from Model
date: 2021-02-11
categories: [laravel, laravel-8, model]
description: Retrieve only the column that you wanted from querying model in Laravel 8.
---

Often times when you are retrieving data from eloquent model, you just need some columns and not all of them.
When using Laravel [eloquent](https://laravel.com/docs/8.x/eloquent) model to query database, Laravel will return a collection instance. That means you get the whole bunch of method available on collection.

Normally you would do like this to get all of the data for a user in users table.

```php
$users = User::where('active', true)->get();
```

But if you only want, let say id and name of the user you can easily do something like this.

```php
$usersData = User::where('active', true)->get(['id','name']);
```

By passing an array to `get` method, Laravel will only return values of columms contained by passing array.
This is very useful and often come in handy when working with eloquent models.
