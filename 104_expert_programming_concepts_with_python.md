# Programming 104 - Expert programming concepts with Python

[< Course overview](https://github.com/Opensource-Academy/programming)  
[< Previous course module](https://github.com/Opensource-Academy/programming/blob/master/103_advanced_programming_concepts_with_python.md)  

<!-- markdown-toc start - Don't edit this section. Run M-x markdown-toc-refresh-toc -->
**Table of Contents**

- [Programming 104 - Expert programming concepts with Python](#programming-104---expert-programming-concepts-with-python)
    - [Introduction](#introduction)
    - [Return](#return)
        - [Returning](#returning)
        - [How Python looks at code](#how-python-looks-at-code)
            - [Line 1](#line-1)
            - [Line 2 and 3](#line-2-and-3)
            - [Line 4](#line-4)
            - [Execution order](#execution-order)
                - [Let's try](#lets-try)
                - [An error inside the function](#an-error-inside-the-function)
                - [An error inside and outside the function](#an-error-inside-and-outside-the-function)
                - [Indents help](#indents-help)
        - [How returns change the flow of code](#how-returns-change-the-flow-of-code)
        - [What return does](#what-return-does)
        - [Order matters](#order-matters)
        - [Flow control and returns](#flow-control-and-returns)
        - [Smart returns](#smart-returns)
            - [Basic: if, else and return](#basic-if-else-and-return)
            - [Better: if and return](#better-if-and-return)
    - [Test yourself](#test-yourself)
        - [Exercise 0: Warming up](#exercise-0-warming-up)
        - [Exercise 1: Return to sender](#exercise-1-return-to-sender)
        - [Exercise 2: Picky](#exercise-2-picky)
        - [Exercise 3: Calculated](#exercise-3-calculated)
        - [Exercise 4: Phoning it in](#exercise-4-phoning-it-in)

<!-- markdown-toc end -->

## Introduction
This course uses the programming language Python to introduce more programming concepts.

This module ends with a series of exercises.

Have fun!

## Return
The previous two courses introduced [functions](https://github.com/Opensource-Academy/programming/blob/master/102_intermediate_programming_concepts_with_python.md#functions) and [methods](https://github.com/Opensource-Academy/programming/blob/master/103_advanced_programming_concepts_with_python.md#methods).

An example of a function would be `print()`. An example of a method would be `.upper()`.

One of the most important features of method and functions is the ability to *return*.

Return is a *keyword* that is exclusively related to functions and methods.

### Returning
So what can we do by using `return` in our code? Well, it's somewhat in the name: whenever Python encounters a `return` statement, it will do exactly *that*: return from the function that had the return in it.

Let's look at another example to make this clearer:

First, let's look at a simple function without a return.
```python3
def greeter(name):
    """Says hello to name"""
    print('Hello '+name+'!')
greeter('James')
```

Running this script would result in the output:
```
Hello James!
```

Let's have a look at what exactly happens when Python reads this code.

### How Python looks at code
When you 'execute' or 'run' (or whatever phrase you prefer) a Python script, Python does a few things that might not seem obvious.

First of all, Python 'reads the entire file from top to bottom'. This statement is both true, and not true.

Lets have a look at how Python would go over the example we just looked at. Let's assume we stored our code in a script called `greeter.py`.

When talking about line numbers, we start counting at 1. As such:

| Line | Code                     |
| :--- | :---                     |
|    1 | def greeter(name):       |
|    2 | """Says hello to name""" |
|    3 | print('Hello '+name+'!') |
|    4 | greeter('James')         |

This is what happens after `python greeter.py`: 

#### Line 1
Line 1 is an interesting one:
```python3
def greeter(name):
```
So the first thing Python will notice is the `def` keyword. Python knows that we're defining a function here, as such, it knows to skip all lines that belong to this function!
#### Line 2 and 3
We already established that line 2 and line 3 are part of the function that we started on line 1.
```python3
    """Says hello to name"""
    print('Hello '+name+'!')
```
Line 2 is the function's *docstring*: you probably already guessed or knew that Python doesn't do anything with this line.

Line 3 is where the actual code that makes our function starts (and ends, because, if we don't count the docstring, our function has only a single line of actual code).

Both line 2 and 3 are initialy not 'executed' by Python.

#### Line 4
Line 4 is where the function is *called*. When Python reaches this line and comes across `greeter('James')` it will finaly look at the code within our function `greeter()`.

#### Execution order
That means that the execution order of our example script comes down to:
```
Line 1
Line 4
(Line 2)
Line 3
```

##### Let's try
You can easily test this yourself by creating a situation that will result in an error.

Let's print an undefined variable x in our script, at various positions.

##### An error inside the function

```python3
def greeter(name):
    """Says hello to name"""
    print(x)
    print('Hello '+name+'!')
greeter('James')
```

Running the above example will result in:

```python3
NameError: name 'x' is not defined
```
So far, so good.

##### An error inside and outside the function
Now we will add another impossible instruction for Python by also adding `print(y)`, but this time, outside of the function.

The `print(x)` part is still in there too. Let's run it and see which error shows up first.

```python3
def greeter(name):
    """Says hello to name"""
    print(x)
    print('Hello '+name+'!')
print(y)
greeter('James')
```

The result:
```python3
NameError: name 'y' is not defined
```

As you can clearly see, Python first caught the error outside of the function.

> What error will Python throw if you swap the `print(y)` and `greeter('James')` lines around?

##### Indents help
One of the reasons for using Python for this programming introduction is Python's way of making blocks of code (with *indents*, also known as *whitespace*).

These indents make it very easy for humans to read Python code, it also makes it very easy for a programmer to know in what order statements will be run.

### How returns change the flow of code
We now know that Python doesn't "look" at all code at once. By making use of returns, we can change the way Python goes through code within functions.

### What return does
A few lines ago, we saw that "return is used to return from the function that had the return in it."

Let's update our example to include a return.
```python3
def greeter(name):
    """Says hello to name"""
    return 'Hello '+name+'!'
greeter('James')
```
Saving the above code to `greeter.py` and running it will result in no output at all; we no longer tell Python to print the result of `greeter()`.

To do something with the result that is returned from our `greeter()` function, we will first have to "catch" the result.

Let's put the result in a variable `result`. If we want to actualy print the contents of `result` we will of course have to tell Python to use `print()`, so let's add that too.
```python3
def greeter(name):
    """Says hello to name"""
    return 'Hello '+name+'!'
result = greeter('James')
print(result)
```
Storing the code in a script and running it will once again result in the output:
```
Hello James!
```
Did you follow what happened?

1. We defined `greeter()`
2. We said that we wanted to run `greeter()`, storing the result in the variable `result`
3. Then we print `result`

### Order matters
Let's focus a bit more on 
```python3
result = greeter('James')
```
When code such as this is ran, it's important to realise that the part to the right of the `=` is executed first. The part left of the `=` is ran last.

If you think that is strange, consider that we could also do something like `x = 8 + 8` to create a variable `x` holding the value `16`. If the statement would be run in any other order, stuff would quickly get confusing (and undoable).

### Flow control and returns
When working with flow control statements such as `if`, it's possible for a function to have more than one return.

Let's look at a simple example. Note that this time, the returned result isn't stored in a variable, instead, `print()` goes around `tester()`. This way, the result still ends up in `print()` and generates output.
```python3
def tester(the_code):
    """Returns True if the_code matches secret, otherwise returns False"""
    secret = 'sekrit!'
    if the_code == secret:
        return True
    else:
        return False
print(tester('what is the secret?'))
```
The output of this script is of course:
```Python3
False
```

### Smart returns
Let's look at the example from last time. There is something "wrong" with the code.

> Think about it for a second, when we use `return` we instantly stop doing whatever our function is doing and return whatever we tell return to send back. So, what line from the example do we really not need at all? (The *docstring* doesn't count!)

Guessed it?

Let's have a look:

#### Basic: if, else and return
This is the "bad" version of the code:
```python3
def tester(the_code):
    """Returns True if the_code matches secret, otherwise returns False"""
    secret = 'sekrit!'
    if the_code == secret:
        return True
    else:
        return False
print(tester('what is the secret?'))
```

#### Better: if and return 
The improved version of the code:
```python3
def tester(the_code):
    """Returns True if the_code matches secret, otherwise returns False"""
    secret = 'sekrit!'
    if the_code == secret:
        return True
    return False
print(tester('what is the secret?'))
```
While this might look like a really minimal difference, there are a few reasons to keep an eye out for improvements like this:

- Less code means less chances for making mistakes
- Less code means easier reading
- In our example, removing the `else` removes another level of indention, which makes reading and working with the code slightly easier.

Train yourself to look out for and improve code like this. It will make you a much more effecient programmer.

## Test yourself

### Exercise 0: Warming up
Write a function `my_function` that takes the arguments `number1` and `number2`, adds them up and then returns the result. Print the result.

### Exercise 1: Return to sender
Write a function `scream()` that takes the argument `target`. `target` should take a string, transform that string to be ALL CAPITALS and add `'!!!'` to your string. Run your function, store the result in a variable `loud` and print the result when you run your script.

If run your script with the string `banana`, the resulting output should be `BANANA!!!`.

### Exercise 2: Picky
Write a function `picker()` that takes the argument `person`. `person` should take a string. 

Test if the value inside `person` matches 'James' or 'Mike'. If it matches 'James' return `'Nerd'`, if it matches 'Mike' return `'who?'`.

You are **not** allowed to use `else`!

### Exercise 3: Calculated
Grab that calculator from the previous exercises. Finish it (or possible rebuild it!) by using functions that make use of `return` (where needed).

### Exercise 4: Phoning it in
Very much like with the previous exercise, use the phonebook from the last module and make it awesome by:
- using smart returns wherever possible
- fixing the remove function: remove deletes entries based on first names, make sure that the function prompts for a last name on duplicate first names
- fixing the remove function even more by asking for an email adress for entries that share first and last names
