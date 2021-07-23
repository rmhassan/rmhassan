---
extends: _layouts.post
section: content
title: List of data structures in python complete guide
date: 2021-07-23
featured: false
description: Different types of data structures in Python. An explanation of lists, sets, dictionaries etc.
---

Data structes are container that organize and store data in different ways. As stated on [wikipedia](https://en.wikipedia.org/wiki/Data_structure)

> A data structure is a data organization, management, and storage format that enables efficient access and modification

We will have a look at data structures in python. Python is very famous for Data Science, Artificial Intelligence, and Machine learning. I have discussed some of the benefits of learning python in another [post](https://www.rmhassan.com/blog/benefits-of-learning-python/).

There are two types of data structures in python

- Builtin data structures
- User defined data structures

#### Builtin Data structures

There are four types of builtin data structures namely list, tuple, sets and dictionary. Let explain each
of them with examples.

##### List

List is the most common and basic data structer. If you have come from other language like javaScript, it is like an array. It can store different data types like integer, float and string.

```python
my_list = [0.1, 5, 'data strucutes']
```

Here `my_list` is a list that contains different data types. But unlike other languages, pthon has a syntax that can be used to slice lists(and any other data collection). For example if you have a list of even numbers.

```python
list_of_even_numbers = [2,4,6,8,10,12]
```

Then you can slice the list by using different index numbers. Let say we want to start from 0 index(like any other language, index starts from zero in python) and go all over to index 3. We can achieve this by writing `list_of_even_numbers[0:4]`.

But keep in mind that the starting value, zero , is inclusive and the ending value, four , is exclusive.
The line of code above will return `[2,4,6,8]`.

It is called slice and dice.

It can have many shapes. Like if you omit first(start) value, it will start from zero, and the same goes for last(end) value. If you omit ending value, the resulting list will have all elements from start up to the last element in the list. e.g
`list_of_even_numbers[:2]` will give you `[2,4]` etc.

Lists are mutable.

> An object(list, string) is called mutable if they or their value can be changed after creation

##### Tuples

Tuples are immutable, and that is the only major thing that makes the difference between tuples and list.
The minor difference is how you create tuples. Tuples are useful when you want to group things that are closely related, like coordinates. e.g `coordinate = (xcoord, ycoord)`

```python
my_tuple = (0.1, 5, 'tuples are immutable')
```

Notice the paranthesis () rather than brackets []. But paranthesis here are optional.

##### Sets

Sets are mutable, unique collection of elements. Notice the word unique, as this makes all the difference. In other words, sets only contain unique values. If you convert a list with duplicates value into a set, it will remove all the duplicates values. This is very useful.

Let's say we have a list of languages spoken by your customers across the world. Now there are people who can speak multiple languages, and there are people that live in same country and as a result speak same language.
So our data will have many duplicate values. If we then convert this list into a set, the duplicate values will be automatically removed and you will end up having unique list of languages spoken by your customers.

Take a look at the example below

```python
my_language_list = ['English', 'Chinese', 'English', 'French','Italian', 'English']
my_language_set = set(my_language_list)
```

Now if we print `my_langugage_set`, we will get `{'English', 'Chinese', 'French', 'Italian'}`. Also notice the curly braces. Set's elements are wrapped in `{}`.

##### Dictionary

Dictionary is mutable collection of key/value paire elements. Keys must be unique. A dicitionary with the key/vlaues of countries and their population will look something like this.

```python
population = {'China':1408,'India': 1379, 'Pakistan': 220, 'USA':330 }
```

It is evident that dictionaries are very useful when you are required to store your data in key/value pairs.

#### User defined data structures

##### Stack

Stack is a linear data structure. In stack, data entered at the last will be accessed first. This is called Last-in-First-out princple.

> A linear data structure have elements in sequence and each element is connected to its previous and next element.

##### Queue

Queue is also a linear data structure but it works on the principle of first-in-first-out; that is the element storeed first will be accessed first.

##### Tree

Tree is a non-linear data structure. Tree will have an element at the root and then all other nodes originate from the root node. Every node after the root node will be called parent and nodes originating from these parent node will be called their child and the process goes on. Tree can have many levels based on how many parent-child pair you have, and the nodes in the last level are called leaves.

There are serveral other data structures that are alos used like Linked list, graph, and hashmap etc.

Now that you have an overview of what data structures are in python, you can practise this on a site like [HackerRank](https://www.hackerrank.com/).

Wish you good luck.
