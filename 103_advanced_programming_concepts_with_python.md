# Programming 103 - Advanced programming concepts with Python

[< Course overview](https://github.com/Opensource-Academy/programming)  
[< Previous course module](https://github.com/Opensource-Academy/programming/blob/master/102_intermediate_programming_concepts_with_python.md)  

<!-- markdown-toc start - Don't edit this section. Run M-x markdown-toc-refresh-toc -->
**Table of Contents**

- [Programming 103 - Advanced programming concepts with Python](#programming-103---advanced-programming-concepts-with-python)
    - [Introduction](#introduction)
    - [Data: Dictionaries](#data-dictionaries)
        - [A simple dict example](#a-simple-dict-example)
        - [Dicts hold other data](#dicts-hold-other-data)
        - [Adding and removing dict elements](#adding-and-removing-dict-elements)
            - [Adding or changing dict elements](#adding-or-changing-dict-elements)
            - [Removing dict elements](#removing-dict-elements)
        - [There is more!](#there-is-more)
    - [Objects](#objects)
        - [Methods](#methods)
            - [Finding methods](#finding-methods)
            - [Using methods](#using-methods)
        - [Methods != functions](#methods--functions)
    - [Classes](#classes)
    - [Test yourself](#test-yourself)
        - [Exercise 0: Start a band](#exercise-0-start-a-band)
        - [Exercise 1: Kick someone out](#exercise-1-kick-someone-out)
        - [Exercise 2: Add a member](#exercise-2-add-a-member)
        - [Exercise 3: Update the band](#exercise-3-update-the-band)
        - [Exercise 4: Split 'em up](#exercise-4-split-em-up)
        - [Exercise 5: Split them some more](#exercise-5-split-them-some-more)
        - [Exercise 5: Show 'em all](#exercise-5-show-em-all)
        - [Exercise 6: Master of methods](#exercise-6-master-of-methods)
        - [Exercise 6: Methods for all](#exercise-6-methods-for-all)
        - [Exercise 7: Join in](#exercise-7-join-in)
        - [Exercise 8: Discriminate](#exercise-8-discriminate)
        - [Exercise 9: The rest isn't that important](#exercise-9-the-rest-isnt-that-important)
        - [Exercise 10: Let's write a phonebook](#exercise-10-lets-write-a-phonebook)
            - [Data variable](#data-variable)
            - [user_add](#useradd)
            - [user_remove](#userremove)
            - [list_users](#listusers)
        - [Exercise 11: Divide](#exercise-11-divide)
        - [Exercise 12: Make it look nice](#exercise-12-make-it-look-nice)
        - [Bonus: Objectively better](#bonus-objectively-better)

<!-- markdown-toc end -->

## Introduction
This course uses the programming language Python to introduce more programming concepts.

This module ends with a series of exercises.

Have fun!

## Data: Dictionaries
The [first course module](https://github.com/Opensource-Academy/programming/blob/master/101_introduction_to_programming_with_python.md#data-numbers-text-and-booleans) introduced the datatypes *string*, *integer* (int), *floating point* (float) and *boolean*. The [previous course module](https://github.com/Opensource-Academy/programming) introduced the datatype *list*.

This chapter will introduce you to the datatype *dictionary*, usualy refered to as *dict*.

Dictionaries are used to map *keys* to *values*. While that might sound scary, it really isn't.

Remember lists? `my_list = ['a', 'b', 'c']`. When we want to retreive data from `my_list` we can use `my_list[0]` to retreive the value `'a'`. This is because in our list example, the value `'a'` is what is stored at the *index* `0`.

Dictionaries work in a similar way, but instead of making use of an index, a *key* is used to retreive data.

### A simple dict example
Let's look at a simple dictionary example:
```python3
my_dict = {'key1': 'value1', 'key2':'value2'}
```
In the example above, we can find the following keys and values:

| Key  | Value  |
| ---  | ---    |
| key1 | value1 |
| key2 | value2 |

Retreiving data from the example dictionary works like this:
```python3
my_dict = {'key1': 'value1', 'key2':'value2'}
my_dict['key1']
```
The resulting output of `my_dict['key1']` would be `'value1'`.

### Dicts hold other data
Lists could hold any other type of data as their value. It is, for example, possible to have a list of lists.

Dicts work very much the same way, dicts can store strings, ints, lists or possibly even dicts.

Have a look at the following example (*note*: you can scroll the example horizontally).

```python3
my_dict = {'my_string': 'this is a string', 'my_int': 8, 'my_float': 8.001, 'my_list': ['apple', 'banana'], 'my_dict': {'my_key': 'my_awesome_value'}}
```

Let's make the above example more readable by slightly changing the formatting.
```python3
my_dict = {
    'my_string': 'this is a string',
    'my_int': 8,
    'my_float': 8.001,
    'my_list': [
        'apple', 
        'banana'
        ],
    'my_dict': {
        'my_key': 'my_awesome_value'
        }
    }
```

> How would one retreive the value `my_awesome_value` out of the above example dict `my_dict`?

### Adding and removing dict elements
Being able to make and read a dict is nice, but sometimes dicts require changes.

#### Adding or changing dict elements
Adding something to a dict is simple. Let's look at how it's done:

```python3
# We have some dict, called 'my_dict'
my_dict = {'a': 'value a', 'b': 'value b'}
# Now we want to add {'c': 'value c'} to "my_dict"
my_dict.update({'c': 'value'})
```

So to add a dict, we use `.update()`. Notice the `()` at the end of update. Remember functions? Very much like we can send arguments to a function, `.update()` requires information in the form of the extra *key* *value* pair that we want to add.

Notice how the new *key* *value* pair is basically a dict too.

> *Note*: using `.update()` on a dict will overwrite existing keys and their value.

#### Removing dict elements

To remove something from a dict we can use `.pop()`, `.pop()` needs a valid key (one of the keys from the dict) to remove something from the dict.

Let's look what using `pop()` looks like in practise:

```python3
# We have some dict, called 'my_dict'
my_dict = {'a': 'value a', 'b': 'value b'}
# Now we want to remove the key and value for 'a'
# Pop will return the value corresponding with the key we just removed
my_dict.pop('a')
'value a'
# Let's see what 'my_dict' looks like now
my_dict
{'b': 'value b'}

```

### There is more!
There are many more things that can be done with and to dicts. However, for now, let's have a look at what exactly happened when we used `.update()` and `.pop()`. This brings us to the next chapter.

## Objects
You might have heard someone say that Python is an 'object oriented language' or even 'everything in Python is an object'. If you haven't, give it some time, you'll see it.

But *what* does all of that mean in practise?

In practise this means that, in Python, all the elements we work with (such as, for example, strings or dicts) have their own build in "functions" called *methods*.

This isn't all there is to say about objects (not at all), but being able to use *methods* and to understand the difference between *methods* and *functions* is rather important.

### Methods

Let's have a look at a simple example object, in the form of a string.

```python3
my_string = 'hello world'
```

#### Finding methods
Strings come with an array of usefull methods, you can use Google to get an overview or, in the case of Python, use Python's `help()` function to get more information. To use Python's build in help, start Python by simply running `python`. Next, use:
```python3
help(str)
```

> Note: Python's help is a "vi-like", you can quit by pressing `q`, search with `/`, or use commands such as `gg` and `G`.

#### Using methods
Functions are ran by calling them, such as in this example:
```python3
print('Hello world')
```

When we talked about dicts, we used `.update()` and `.pop()`, these are examples of dict methods.

Methods are called by using the `.` (dot) and then the method name. Much like with functions, methods also require `()` (parenthesis). In the case of the dict method `.pop()` we saw that we had to give `.pop()` the key that we wanted to remove from the dict.

Let's look at some *methods* that can be found on all Python strings.

```
# Our base string, stored in the variable "string"
string = 'Hello World'

# Let's use an obvious method: upper()
string.upper()
'HELLO WORLD'

# We can also do the opposite
string.lower()
'hello world'

# With split(), we can split a string on every occurence of the string that we send in.
# In this example, we split the string in the variable "string" at the string " ".
# Note how the result comes in a list
string.split(' ')
['Hello', 'World']

# A more complex split example would be:
string = 'Jon|jon@internet.com|Banana Road 20|Some place|Planet Earth'
string.split()
['Jon', 'jon@internet.com', 'Banana Road 20', 'Some place', 'Planet Earth']
```

`upper()`, `lower()` and `split()` are just a few examples of all available string methods (in Python!).

### Methods != functions
While we could say that methods are basically functions for objects, it's important that you are able to spot the difference.

The `.` (dot) notation makes it very easy to spot the difference.

## Classes
While discussing objects, we only looked at build in objects. You might have guessed that it is also possible to build you own objects, in Python, these are refered to as a *class*.

Classes are often called 'objects' by other programmers. If you plan to continue using Python, make sure to use the right word from now on when talking about *classes*, because remember, "everything is an object", so calling something an object doesn't provide others with a lot of useful information.

Python classes will be covered in the Python course. For now it's simply important that you realise that it's possible to define your own objects in object oriented languages.

## Test yourself

### Exercise 0: Start a band
Turn the table below into a Python dict stored in the variable `band`.
Oh and print it, by now, that should be easy.

| key    | value |
| :---   | :---  |
| drums  | Lars  |
| vocals | James |
| guitar | Dave  |

### Exercise 1: Kick someone out
Use the `band` dict from the previous exercise. 
Remove `'Dave'` from the dict. 
Store the new version of the dict in the `band` variable again.

### Exercise 2: Add a member
Use the `band` dict from the previous exercise. 
Update the dict in `band` to include `{'guitar': 'Kirk', 'bass': 'Cliff'}`
Print your new `band` variable.

### Exercise 3: Update the band
Use the `band` dict from the previous exercise. 
Update the dict in `band` so `{'bass': 'Cliff'}` is updated to `{'bass': Jason}`.
Print your new `band` variable.

### Exercise 4: Split 'em up
Use the string method `.split()` to turn this string:
```python3
my_band = 'Lars James Kirk Cliff'
```
Into this list:
```python3
['Lars', 'James', 'Kirk', 'Cliff']
```
Print your list.

### Exercise 5: Split them some more
Use the string method `.split()` to turn this string:
```python3
my_band = 'Lars, James, Kirk, Cliff'
```
Into this list:
```python3
['Lars', 'James', 'Kirk', 'Cliff']
```
Print your list.

### Exercise 5: Show 'em all
Use the string method `.split()` to turn this string:
```python3
my_band = 'Lars:James:Kirk:Cliff'
```
Into this list:
```python3
['Lars', 'James', 'Kirk', 'Cliff']
```
Use a `for` loop to print every name on a new line.

### Exercise 6: Master of methods
So far we used string and dict methods. Let's do something with list methods.

Use this list of ints:
```python3
unsorted_years = [2003, 1986, 2008, 1983, 1997, 1996, 1988, 1991, 2016, 1984]
```
Using a list method, use a single line of code to sort this list of years.

### Exercise 6: Methods for all
Use this list of ints:
```python3
unsorted_years = [2003, 1986, 2008, 1983, 1997, 1996, 1988, 1991, 2016, 1984]
```
Store a sorted list of years in the variable `sorted_years`.
Print the original `unsorted years` list. Print the `sorted_years` list.

What did you just learn about variables? (If you hadn't noticed yet, compare your `unsorted_years` with the `unsorted_years` in this exercise!)

### Exercise 7: Join in
Look at this example using the `.join()` method.
```python3
some_words = ['Hello', 'I', 'am', 'learning', 'to', 'program']
print(' '.join(some_words))
```

The result of the above code is:
```
Hello I am learning to program
```

Use the `join()` method to turn the list below into a string. Elements should be seperated by `:`.

Use:
```python3
user_data = ['Cliff', 'Burton', '1962', '1986', 'Bass']
```
Store the result in a variable named `member`, print `member`.

The result of the print should look like this:
```
Cliff:Burton:1962:1986:Bass
```
### Exercise 8: Discriminate
Have a look at this list of words:
```
word_list = [
    'MASTER',
    'Justice,
    'RIDE,
    'load,
    'Garage',
]
```

Use the list as provided above (you can copy paste it).
Use a `for` loop to loop over the list.
Use string methods to only print words that are printed in CAPITALS **only** or small letters **only**.

### Exercise 9: The rest isn't that important
Have a look at this list of words:
```
word_list = [
    'MASTER',
    'Justice,
    'RIDE,
    'load,
    'Garage',
]
```

Use the list as provided above (you can copy paste it).
Use a `for` loop to loop over the list.
Store all entries that use mixed casing (both upper and lower) in a list. Store the list in the variable `else`.
Store all entries that use UPPER casing in a list. Store the list in the variable `matters`.
Store all entries that use lower casing in a list. Store the list in the variable `nothing`.

Print 'Nothing:', loop over the list in `nothing` and print every result to a new line.
Print 'Else:', loop over the list in `else` and print every result to a new line.
Print 'Matters:', loop over the list in `matters` and print every result to a new line.

### Exercise 10: Let's write a phonebook
Calculators are fun, but this time, we'll write something else. A phonebook (if you don't know what a phonebook is, a phonebook is very much like the contacts app on your phone, but in print, so it updates slowly).

The phonebook requires a few things.

- A `data` variable. This should be a list.
- A `user_add()` function. Which you will write yourself.
- A `user_remove()` function. Which you will write youself.
- A `list_users()` function. Which you will write yourself.

Phonebook entries require some kind of setup. Structure your entries in dicts like this:

```python3
{'name_first': '', 'name_last': '', 'email': '', 'phone': ''}
```
Note how all values in the dict are strings, this will make working with the data much easier.

#### Data variable
The `data` variable should simply be a list. In this list we will be storing user data. Every user will get their own dict.

#### user_add
The `user_add` function should update the list in `data` to include a new user_dict (as described above).

Your function should accept four arguments: `name_first`, `name_last`, `email` and `phone`.

Your function should return the new user dictionary.

#### user_remove
The `user_remove` function should remove a user from the list in `data`. Use a `for` loop or look up an alternative method to find users in the list based on their first name.

#### list_users
The `list_users` function should return a list of all users. Use a `for` loop or look up an alternative method to list all users. Be sure to print all userdata (`first_name`, `last_name`, `email` and `phone`).

Aim for an output that is similair to:
```
First name: Bob
Last name: Ross
email: bob@ross.mail
phone: 555666777888
```

### Exercise 11: Divide
Reuse the code from the previous exercise.

Do the exact same thing, but make your output look like this:

```
--------------------
First name: Jon
Last name: Ross
email: bob@ross.mail
phone: 555666777888
--------------------
First name: Son
Last name: Goku
email: songoku@dragon.balls
phone: 555444333222
```

### Exercise 12: Make it look nice
Use the code from the previous exercise.
When printing results, use the `len()` function to make sure that all the dividers (`---`) are the same length. Use the lenght of the longest line you are printing to decide the maximum ammount of `-` to use.

The example above would then look like this:
```
---------------------------
First name: Jon
Last name: Ross
email: bob@ross.mail
phone: 555666777888
---------------------------
First name: Son
Last name: Goku
email: songoku@dragon.balls
phone: 555444333222
```

### Bonus: Objectively better
Using dicts and lists is fun. But doing the same thing with classes is much more efficient. If you are about to continue learning Pyhon, build the phonebook from exercises 10-12, this time, using a python class.

Start off by finding out how to write your own classes.

Turn the phonebook functions into methods.
