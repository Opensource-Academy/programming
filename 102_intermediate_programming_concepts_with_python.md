# Programming 102 - Intermediate programming concepts with Python

[< Course overview](https://github.com/Opensource-Academy/programming)  
[< Previous course module](https://github.com/Opensource-Academy/programming/blob/master/101_introduction_to_programming_with_python.md)  

<!-- markdown-toc start - Don't edit this section. Run M-x markdown-toc-refresh-toc -->
**Table of Contents**

- [Programming 102 - Intermediate programming concepts with Python](#programming-102---intermediate-programming-concepts-with-python)
    - [Introduction](#introduction)
    - [Data: Lists](#data-lists)
        - [Simple list example](#simple-list-example)
        - [Collections of values](#collections-of-values)
        - [List notation](#list-notation)
        - [Getting data out of lists](#getting-data-out-of-lists)
            - [Backwards!](#backwards)
            - [Slices](#slices)
                - [Advanced slicing](#advanced-slicing)
            - [Nested lists](#nested-lists)
            - [Out of range](#out-of-range)
        - [Changing lists](#changing-lists)
        - [List functions](#list-functions)
        - [Working with lists](#working-with-lists)
            - [Iteration](#iteration)
            - [Combining](#combining)
        - [Finally](#finally)
    - [Functions](#functions)
        - [What is a function?](#what-is-a-function)
        - [Defining a functions](#defining-a-functions)
        - [Function arguments](#function-arguments)
        - [Basic return](#basic-return)
        - [Function docstrings](#function-docstrings)
        - [Where are functions used?](#where-are-functions-used)
            - [Writing the same code over and over again is a waste of time](#writing-the-same-code-over-and-over-again-is-a-waste-of-time)
            - [Writing the same code over and over again leads to mistakes](#writing-the-same-code-over-and-over-again-leads-to-mistakes)
            - [Writing the same code means having to update the same code over and over again](#writing-the-same-code-means-having-to-update-the-same-code-over-and-over-again)
            - [Functions to the rescue](#functions-to-the-rescue)
    - [Test yourself](#test-yourself)
        - [Exercise 0:](#exercise-0)
        - [Exercise 1: Make a list](#exercise-1-make-a-list)
        - [Exercise 2: Combine a list](#exercise-2-combine-a-list)
        - [Exercise 3: Looping](#exercise-3-looping)
        - [Exercise 4: Laugh at cats](#exercise-4-laugh-at-cats)
        - [Exercise 5: Say hello](#exercise-5-say-hello)
        - [Exercise 6: Say hello to someone](#exercise-6-say-hello-to-someone)
        - [Exercise 7: Say hello to the cats](#exercise-7-say-hello-to-the-cats)
        - [Exercise 8: Function fixing](#exercise-8-function-fixing)
        - [Exercise 9: the final argument](#exercise-9-the-final-argument)
        - [Exercise 10: Fix 'er up!](#exercise-10-fix-er-up)

<!-- markdown-toc end -->

## Introduction

This course uses the programming language Python to introduce more programming concepts.

This module ends with a series of exercises.

Have fun!

## Data: Lists
The [previous course module](https://github.com/Opensource-Academy/programming/blob/master/101_introduction_to_programming_with_python.md#data-numbers-text-and-booleans) introduced the datatypes *string*, *integer* (int), *floating point* (float) and *boolean*.

This chapter will introduce you to the datatype *list*.

Lists are exactly what you think of when you hear the word 'list': an ordered collection of values.

A list of programming languages:
```
bash
python
go
```

### Simple list example
Python uses the square brackets (`[]`) to create lists. A simple list in Python could look like this:
```python3
[1, 2, 3, 4, 5]
```

Creating a list is easy:
```python3
numbers = [1, 2, 3, 4, 5]
```

### Collections of values
We can fit all kinds of data in lists:
```python3
# List of names (strings)
names = ['Jimmy', 'Jon', 'Sean']

# List of booleans
bools = [True, False, True, False, False]

# Mixed list
user_date = ['Suzie', 20, False, '55527492233']

# A list of lists
my_lists = [[1,2,3], [True, False, True], ['Jimmy', Jon', 'Sean']]

# A list using variables
a = 1
b = 2
c = 3
var_list = [a, b, c]
```

### List notation
To improve readability, lists can also be written out like this:
```python3
# List of names (strings)
names = [
    'Jimmy', 
    'Jon', 
    'Sean'
]
```

### Getting data out of lists
Get data out of a list by using suqare brackets (`[]`).
```python3
# Make a list
my_list = ['a', 'b', 'c']
# Read from list
my_list[0]
```

`my_list[0]` returns `'a'`.
The above example takes list element `0` from the list `my_list`. The first element of a list is always on position `0`. Therefore, we can say that, at least in Python, lists are *zero-indexed*.

#### Backwards!
It's also possible to call indexes in reverse.
```python3
my_list = [0, 1, 2]
my_list[0]
0
my_list[-1]
2
```

#### Slices
It's also possible to retreive more than one single value at a time. These collections are called *slices*. Slices are also returned as a list.

```python3
my_list = ['a', 'b', 'c', 'd', 'e']
my_list[2:4]
['c', 'd']
```

Note how in the example, retreiving `my_list[2:4]` only returns the values indexed at position `2` and `3`. This is because `my_list[2:4]` means that we ask Python to return the values from `my_list`, starting at index `2` *up to, but not including* `4`.

##### Advanced slicing
Try the following examples and see what they do:
```python3
my_list = ['a', 'b', 'c', 'd', 'e']
my_list[:3]
my_list[3:]
my_list[-3:]
```

#### Nested lists
In one of the previous examples, we used a list of lists. Getting data from a list in a list works exactly the same way as with non-nested lists:
```python3
my_lists = [['a', 'b', 'c'], [1, 2, 3]]
```
Calling `my_list[0][0]` will return `'a'`.

#### Out of range
Trying to read from a non-existing index will generate an `IndexError` in Python.
```python3
IndexError: list index out of range
```

### Changing lists
Updating a list is easy. Simple update the index you want to change.
```python3
my_list = ['Jimmy', 'Jon, 'Sean']
my_list[1] = 'Joe'
my_list
['Jimmy', 'Joe', 'Sean']
```

### List functions
There are several functions that work very well with lists. Some usefull examples are:

| Function | Description                            |
| ---      | ---                                    |
| len()    | Returns the length of a list, as *int* |
| sorted() | Returns a sorted version of the list   |

### Working with lists

#### Iteration
In Python, it's very easy to 'loop' over an entire list.
```python3
cats = ['Jimmy', 'Sean', 'Jon']
for cat in cats:
    print(cat)
```
The output would be:
```
Jimmy
Sean
Jon
```

#### Combining
In Python, it's very east to combine two lists:
```
my_list = [1,2,3] + [4,5,6]
```

The output for `print(my_list)` would be `[1,2,3,4,5,6]`.

### Finally
This chapter barely described the basics of lists. Consult your programming languages documentation to find out what datatype equals or comes closest to Python's *list*.

## Functions
So far, this course has referenced several functions, including, but not limited to `print()` and `input()`.

### What is a function?
Simply put, a function is a collection of code that you want to easily re-use again.

### Defining a functions
In Python, functions are defined using the `def` keyword.

Creating a new function called `my_function` that runs `print(8)` would look like this:
```python3
def my_function():
    print(8)
```
Calling this function comes down to:
```python3
my_function()
```

### Function arguments
Note the `()` at the end of the function. If we want to pass any arguments to our function, we can define those here.

Functions that take no arguments still require the `()` when both defining and calling the function.

Let's look at an example function with an argument. The function `hello_you` takes one argument `name` and then prints a message.
```python3
def hello_you(name):
    print("Hello "+name)
```
When the funtion is used:
```python3
hello_you('Sarah')
Hello Sarah
```

### Basic return
Much like we can send data to a function with arguments, functions can also *return* data.

A very simple example of a return would be:
```python3
def first_letter(word):
    '''returns the first letter of word'''
    first = word[0]
    return first
```

Returned data can be used like any other data. For example, assigning to a variable or printing:
```python3
first = first_letter('Sarah')
print(first_letter('Sarah')
```

Returns are covered more thouroughly in part 4 of this course.

### Function docstrings
Remember the previous module's entry on [comments](https://github.com/Opensource-Academy/programming/blob/master/101_introduction_to_programming_with_python.md#comments)? Function's have their own special place for comments. This so called 'doc string' consists of usefull information about the function.

A simple example:
```python3
def hello_you(name):
    '''Print hello and the supplied name '''
    print("Hello "+name)
```

### Where are functions used?
Let's look at a practical example:

You need to add up 2 numbers, multiply them by 500 and then print the result.

In a scenario where you need to to this with the numbers `100 & 200` and `300 & 400`, you could simply write a script like this:

```python3
result = (100+200)*500
print(result)
result = (300+400)*500
print(result)
```
Easy enough! But what happens if you need to do this to a collection of a 100 of these pairs. Or a 1000, or milion?

While it would still be possible to do this by hand, writing a function is a better idea:

#### Writing the same code over and over again is a waste of time
Just like the title says: writing the same code is boring and not worth your time.

#### Writing the same code over and over again leads to mistakes
Writing something hundreds of times will lead to fatigue. Finding a single mistake in 1000 lines of code is, once again, a waste of time.

#### Writing the same code means having to update the same code over and over again
Just imagine what would happen if the requirements in the example scenario would change. Let's say we no longer times by 500, we now need to multiply by 601. Updating 1000 lines of code is, you guessed it, a massive waste of time.

#### Functions to the rescue
Let's have a look at how the example from above could translate to a function.

```python3
def my_formula(number_1, number_2):
    '''Add up n_1 and n_2, times the result by 500 and print the final result'''
    result = (number_1+number_2)*500
    print(result)
```

## Test yourself

### Exercise 0: Make a list
Make a list out of the following strings:
```
bash
python
go
```
Print your list.

### Exercise 1: Print a list
Use this list: `the_list = ['Jim', 'Jon', 'Sean']`. Write a script that uses the list and then prints `Sean`.

### Exercise 2: Combine a list
Using the list from the previous exercise, extend the list with this list `the_other_list = ['Suzie', 'Rachel', 'Joe']` and store your extended list in the variable `new_list`.

Print the results of `new_list`.

### Exercise 3: Looping
Use this list: `cats = ['Jim', 'Jon', 'Joe', 'Sean']`. Use a `for` loop to print every name on the list on a seperate line.

### Exercise 4: Laugh at cats
Use this list: `cats = ['Jim', 'Jon', 'Joe', 'Sean']`. Use a `for` loop to write a script that prints `I laughed at `+*NAME* for all names on the `cats` list. (Ex: `I laughed at Jim`).

### Exercise 5: Say hello
Write a function called `hello`. Your function should print `Hello world` whenever it is called.

### Exercise 6: Say hello to someone
Write a function called `hello`. Your function should take the argument `name`. Your function should print `Hello `+*NAME* whenever it is called.

### Exercise 7: Say hello to the cats
Write a function called `hello`. Your function should take the argument `name`. Your function should print `Hello `+*NAME* whenever it is called. Use this list: `cats = ['Jim', 'Jon', 'Joe', 'Sean']`. Use a `for` loop and your `hello` function to say hello to all the cats on the list.

### Exercise 8: Function fixing
Look at this function:

```python3
def formula(x,y):
    '''Prints the result of (x+y)*500* '''
    result = (x+y)*500
    print(result)
    
```
Change the function so it's possible to change the value (currently 500) we times `x+y` by.

### Exercise 9: the final argument
Write a function that does the same thing you did in the previous exercise. Your function takes two numbers, adds them together and multiplies the result with a third value. The result is printed. This time, your function is only allowed to take a single (1) argument. (*Pro-tip:* lists)

### Exercise 10: Fix 'er up!
Remember the [calculator from the previous module](https://github.com/Opensource-Academy/programming/blob/master/101_introduction_to_programming_with_python.md#exercise-11-finish-it)? Make your calculator better by writing functions for it's basic operations (`+`, `-`, `/` and `*`).

[Next course module >](https://github.com/Opensource-Academy/programming/blob/master/103_advanced_programming_concepts_with_python.md)

```
   Copyright 2018 Opensource Academy

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
```
