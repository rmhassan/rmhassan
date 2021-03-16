---
extends: _layouts.post
section: content
title: Convert datetime string to  carbon instance with laravel eloquent
date: 2021-02-24
categories: [laravel, laravel-8, php, eloquent, carbon, datetime]
featured: false
description: Cast your datetime string to carbon instance when querying with laravel eloquent.
---

Recently I was working on a project, where after querying the database via eloquent I get back a datetime string. I wanted to convert it in to timestamp.

To my surprise, converting default `created_at` column to a timestamp was simple. Just by calling `created_at->getTimestamp()` I got the number of seconds since 1970(as far as I remember this is the base year. i.e seconds from 1970 to current time).
But when I tried `my_other_column->getTimeStamp()`, I got an error.
`Trying to call method getTimeStamp() on a string.`
After some googling I understand that Laravel cast created_at and updated_at columns to carbon instance on its own. So if I have to do this for any other column, I have to cast it myself.
And it is very simple. You have to specify a property on model class.
Like so,

```php
protected casts = [
    'my_other_column' => 'datetime:Y-m-d'
];
```

You can add as many columns as you want and of course customize the format as well.
Now whenever querying your database, you will get back a carbon instanse datetime with specified format.
But if you want all of you model's dates to do the same you can do so like this.
This is the example from laravel documentation.

```php
protected function serializeDate(DateTimeInterface $date)
{
    return $date->format('Y-m-d');
}
```
