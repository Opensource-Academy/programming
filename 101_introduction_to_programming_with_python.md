# Programming 101 - Basic programming introduction with Python
<!-- markdown-toc start - Don't edit this section. Run M-x markdown-toc-refresh-toc -->
**Table of Contents**

- [Programming 101 - Basic programming introduction with Python](#programming-101---basic-programming-introduction-with-python)
    - [Introduction](#introduction)
    - [Setup](#setup)
        - [(Programming) language](#programming-language)
            - [What is programming?](#what-is-programming)
            - [Giving instructions](#giving-instructions)
            - [Computers can't think](#computers-cant-think)
            - [Learn to speak their language](#learn-to-speak-their-language)
        - [Python](#python)
            - [Usage: Python scripts](#usage-python-scripts)
            - [The python shell](#the-python-shell)
        - [Versions](#versions)
        - [Getting Python](#getting-python)
        - [Finding Python](#finding-python)
        - [Running Python](#running-python)
        - [Recap](#recap)
    - [Code: A basic breakdown](#code-a-basic-breakdown)
    - [Data: numbers, text and booleans](#data-numbers-text-and-booleans)
        - [Value and type](#value-and-type)
        - [Text: Strings](#text-strings)
        - [Numbers: Ints and floats](#numbers-ints-and-floats)
            - [Integers (int)](#integers-int)
            - [Floating Point (float)](#floating-point-float)
        - [Booleans](#booleans)
        - [Recap](#recap-1)
    - [Operators: operators and operands](#operators-operators-and-operands)
        - [Operators and operands](#operators-and-operands)
        - [List of Operators](#list-of-operators)
        - [Operator precedence](#operator-precedence)
        - [Recap](#recap-2)
    - [Expressions: valid and invalid expressions](#expressions-valid-and-invalid-expressions)
        - [Basic examples:](#basic-examples)
            - [Valid expressions](#valid-expressions)
            - [Invalid expressions](#invalid-expressions)
    - [Statements](#statements)
    - [Variables: defining and naming](#variables-defining-and-naming)
        - [Assignment](#assignment)
        - [Type](#type)
        - [Usage](#usage)
        - [Variable names](#variable-names)
            - [Readability](#readability)
            - [Keywords](#keywords)
    - [Data conversion](#data-conversion)
        - [str()](#str)
        - [Caution](#caution)
    - [Comments](#comments)
        - [The 'hashtag' or 'pound'](#the-hashtag-or-pound)
        - [Easy comment blocks](#easy-comment-blocks)
        - [Where to comment](#where-to-comment)
        - [Disabling code](#disabling-code)
    - [Flow control: if, else and elif](#flow-control-if-else-and-elif)
        - [Branching; flow of control](#branching-flow-of-control)
        - [If / else](#if--else)
        - [Comparing](#comparing)
        - [Elif](#elif)
    - [Loops: while](#loops-while)
        - [Iteration / loops](#iteration--loops)
        - [While](#while)
    - [Input](#input)
    - [Imports](#imports)
    - [Test yourself](#test-yourself)
        - [Exercise 0: Define a variable](#exercise-0-define-a-variable)
        - [Exercise 1: Print it](#exercise-1-print-it)
        - [Exercise 2: Greetings!](#exercise-2-greetings)
        - [Exercise 3: The age old question](#exercise-3-the-age-old-question)
        - [Exercise 4: Combo](#exercise-4-combo)
        - [Exercise 5: Which one?](#exercise-5-which-one)
        - [Exercise 6: Other!](#exercise-6-other)
        - [Exercise 7: Wrong!](#exercise-7-wrong)
        - [Exercise 8: Reading is important](#exercise-8-reading-is-important)
        - [Exercise 9: A simple calculator](#exercise-9-a-simple-calculator)
        - [Exercise 10: Almost a full calculator](#exercise-10-almost-a-full-calculator)
        - [Exercise 11: Finish it](#exercise-11-finish-it)
        - [Bonus 1: Oneliner](#bonus-1-oneliner)
    - [Further reading](#further-reading)

<!-- markdown-toc end -->

## Introduction

This course uses the programming language Python to introduce you to the basics of programming.

This module ends with a series of exercises: you will write you first real Python code.

This guide tries to be as complete as possible whilst also being as short as possible. That means that every line and example is there for a reason.

This guide also aims to be accessible to anyone who completed all of the courses listed in the course's requirements.

Have fun!

## Setup
### (Programming) language
Let's start this course with a simple question: 

#### What is programming?
Simply put, programming is telling a computer what it has to do. Or, put slightly nicer; giving instructions to a computer.

#### Giving instructions

Telling another human being how to do something is not always easy, surely you have been in some sort of misunderstanding with someone before?  
Luckily for humans, humans can come up with their own ideas and draw their own conclusions: telling someone to `bring me that` usually works; unless the amount of things that could have possibly been indicated by 'that' is too large. In that case, the other person might respond with `which one?`. Do you see with how little information humans can communicate effectively?

#### Computers can't think

Computers don't have brains, therefore they *can't* think or draw their own conclusions. Even worse, computers can't do anything unless someone tells them what to do and exactly how to do it.

Think about this: because a computer can only do what it is told, a computer cannot do anything wrong. It can, however, receive bad instructions.

#### Learn to speak their language

Very much like with humans, you need to be able to speak the same language before you can communicate with a computer.

Programming languages are a bit different from human languages though, let's look at a piece of example code that will work in most programming languages:
```
3 + 4
```
Did you understand that? Great, you have what it takes to learn at least some basic programming.

This course uses a programming language called `Python`. Python was chosen because it's rather simple to read and write. You will need to learn just a few basic concepts to be able to write your first code. These concepts are transferable to other programming languages!

### Python

#### Usage: Python scripts
Python is a programming language that was designed to be easy to use. You can write so called *scripts*: little (or big) text files. In these text files are lines of so called code. These text files are called a script because they basically are a list of instructions for the computer. The computer goes over them and does what it is told.

>*Note:* Much like computers, a lot of human jobs involve scripts too: they instruct workers on what to do in what order

Consider this: in film or theater, actors also use a script that tells them exactly what to do and say. Actors go through the script line by line and do what the script tells them to do.

Python scripts are usually saved with the *file extension* `.py`, making it easy to understand for both humans and computers that a file is a Python script.

#### The python shell
To make getting started with Python even easier, it is also possible to run Python in it's so called *interactive shell* mode. If you start this mode from Bash, your terminal will read every line you enter as a line of Python code. 

>*Note:* You can use the interactive shell to try out the first examples in this module.

Python might have been designed to be easy, there is one thing that you need to be aware of before you can start.

### Versions
Python comes in 2 versions: 
- Python 2: the outdated version of Python that will very soon stop receiving updates/support.
- Python 3: the latest and greatest form of Python.

With Python 2 reaching *EOL* (end of life) status soon, you will only focus on Python version 3. However, you need to be aware of the following:

- Be careful of older entries online; back when there wasn't any Python 3, programmers could only write Python 2.
- Some people will tell you that using Python 2 is in some way better: these people are wrong.
- Some computers have several Python versions installed, always be aware what version is used by the `python` command.

### Getting Python
Much like you, a computer has to learn about a new language before it can use it. Unlike you, a computer is able to use a language once you installed it on the machine. Installing everything you need to be able to use a new programming language is usually not very different from installing other software, like a web browser. Various operating systems come with various programming languages pre-installed, so don't install anything just yet.

### Finding Python
Depending on your computer, your machine might have Python 3 installed on it already. Before installing a new version of Python, find out whether or not your computer already has some form of Python installation on it.

>*Note:* If you find yourself with a terminal that says `>>>`, you are in the *interactive Python shell*. If you did happen to end up in the interactive python shell, enter the following command to go back to your regular terminal:
```python3
exit()
```

To find out whether or not Python is installed on your machine, run: (note the capital "V")
```bash
python -V
```
If Python was already installed on your system you should see which version of Python you are currently running.

If Python was not installed on your system you should see an error.
> *Note:* Your machine might come with both Python 2 and Python 3 installed. If `python -V` told you that you are running Python 2, try running `python3 -V` and see what happens!

This guide is based on Python 3.6, the latest version of Python at the time of writing, if you have an older installation or no installation at all you can download Python from https://www.python.org/downloads/

**Remember to grab the latest 3.6 or higher!**

### Running Python
> **Warning:** If you already had Python 2 on your machine and have now installed Python 3 alongside Python 2 *or* your machine came with both Python 2 and Python 3, make sure to use the right Python command; typing `python` into your terminal will open the interactive python shell running python 2, since you want to run Python 3 you should use the following command to start it:
```
python3
```
>*Note:* If you see code examples in this course that require you to run `python` in your terminal and your `python` command starts python 2, make sure to run `python3` instead of just `python`!

Now that you have a working Python 3 install and you know where to find it, run your `python` or `python3` command to open the interactive shell to type along with the rest of this module.

If you use the same command with the filename of a python script, python will try to run the script. Say your python command is `python3` and you have a script called `helloworld.py`, you would run this script by typing `python3 helloworld.py`. The `python` command takes a path to a file, just like `cat` or `vim` would. 

### Recap
You have learned that:
- You need to learn a new language to talk to a computer: a *programming language*
- You need to give a computer instructions, because computers cannot think for themselves
- You will learn how to give a computer instructions with a programming language called *Python*
- A file with lines of Python code in it is called a *script*
- Python comes in 2 versions, version 2 and version 3, only use version 3, but be aware of version 2
- Start Python's *interactive shell* by running the `python` or `python3` command (depending on system setup)
- Run a Python script by running `python scriptname.py` or `python3 scriptname.py`.

## Code: A basic breakdown
Before you can write any sort of code, you will need a basic understanding of what code is.

You already learned that code means instructions for a computer.

Before you can give an instruction, let's have a look at what kind of information you need to be able to give a good instruction.

Let's reuse the example from before:
```
3+4
```
Let's break this code down: there is a number (3), the '+'-sign and another number (4). So in total, you have 3 'parts' in our code, let's call these elements for now.

| element A | element B | element C |
| ---       | ---       | ---       |
| 3         | +         | 4         |

You might have already concluded this yourself, but Elements A and C are both numbers and the '+' is what you want the computer to do with these numbers.

So in short: the code example above *instructs* a computer to add up (element B) the *data* that you give it; element A and element C.

The next chapters explore this much further and will teach you the right terminology.

>*Note:* Try to remember most of this terminology as fast as possible, it will make programming **much** easier.

## Data: numbers, text and booleans

In the `3+4` example you already found out that the `3` and `4` are numbers. Numbers are a type of *data*. Let's talk data.

### Value and type
Data has a **value** and a **type**.

Example:
```python3
8
```
The **value** in the above example is 8 (which you probably already guessed). The type of 8 would be **integer**. Data has exactly **1** type associated with it.

In Python, the four most basic datatypes are **strings**, **integers** (or *ints*), **floating points** (or *floats*) and **booleans** (or *bools*).

Let's go over these datatypes one by one.

### Text: Strings
Strings is how you store text in Python. You can make a *string* by adding quotations marks (' ' or " ") around text. Be sure to use the same kind of quotes at the beginning and end of your string; if you open with single quotes ('), you should close with single quotes ('). 

> *Note:* Strings are of the type *string*.

The most basic example of a string:
```
"Hello World"
```
| data          | type   | value         |
| ---           | ---    | ---           |
| 'Hello World' | string | 'Hello World' |

> Think about it: How would you use a quotation mark inside of a string?

### Numbers: Ints and floats
For numbers, there is more than one data type.
#### Integers (int)
The *integer* type, which simply means round numbers (a 'whole' number).
Example:
```
5
```
#### Floating Point (float)
The *floating point* type, which is for numbers with a full stop (`.`).
```
1.23
```
| data          | type   | value         |
| ---           | ---    | ---           |
| 'Hello World' | string | 'Hello World' |
| 5             | int    | 5             |
| 1.23          | float  | 1.23          |

### Booleans
Where strings, ints and floats can have any possible value (fitting the datatype), the *boolean* type can have only 1 out of 2: a boolean is **either** *True* **or** *False*
> *Note:* Notice how there are no quotation marks around True or False.
> *Note:* Notice the capital *T* and *F* in True and False.

### Recap
- Data has a *type* and a *value*
- Data can come in the **types** *string*, *integer*, *floating point* or *boolean*

## Operators: operators and operands
Now that you have data, you want to do something with or to it. Let's start with a simple *operation*; some very basic maths.  

Example:
```
4 + 5
```
In this example there are 2 *values*, `4` and `5`. You already know that these values are of the *type* integer.  

### Operators and operands
You already know that the `+` in the example takes the values `4` and `5` and then combines them.

The `+` in the example is what's called an **operator**. Operators are special symbols that do something to the values you use them with, these values are called **operands**. In the case of `+` it adds up the values to the left and right of itself, so `+` is the operator and `4` and `5` are it's operands.

> So in short, **operators** operate on **operands**.

### List of Operators

| Operator | Meaning                           | Example 1 | Returns | Example 2 | Returns |
| :---:    | :---                              | :---      |    :--- | :---      |    ---: |
| +        | Addition                          | 3+4       |       7 | 1.5+1.5   |     3.0 |
| -        | Subtraction                       | 7-2       |       5 | 10-20     |     -10 |
| *        | Multiplication                    | 4*3       |      12 | -3\*-3    |       9 |
| /        | Division                          | 25/5      |       5 | 5/5       |     1.0 |
| \*\*     | Exponent                          | 3\*\*3    |      27 | 3\*\*4    |      81 |
| //       | Integer division/floored quotient | 32//5     |       6 | 35//5     |       7 |
| %        | Modulus/remainder                 | 25%10     |       5 | 29%10     |       9 |

### Operator precedence
Operator's are usually handled like you are used to from basic maths classes, if this is new to you: the operator that is **lowest** on the list above goes **first**:

Example:
```
3 + 4 * 5
```
In the above example `4 * 5` will be executed **first** The `3+` part will be executed **last**  
If you want to calculate the `3 + 4` part first, use parentheses `()`, like in the example below:
```
( 3 + 4 ) * 5
```
In this example, the computer would calculate the `3+4` part `first`, so you would end up with 7. Then the machine calculates `7 * 5`, which the computer will do **last**.

### Recap
- There are more operators than listed above, but for now you can recognise an **operator** and it's **operands**.
- You can already do all kinds of maths and calculations with Python.
- You now know how Python handles data and how to do something with said data.

## Expressions: valid and invalid expressions
Now that you have operators and values you can combine these two to form **expressions**.  

The most basic form of an expression is:
**Operand - operator - operand**  
Example:
```
3  +  4
```
### Basic examples:
#### Valid expressions
These will work, so called **valid** expressions:
```
8+8
4*8
"hello"
"hello"+"world"
```

> *Try it:* Be sure to try the last example in the Python shell to see what the `+` operator can do.

#### Invalid expressions
This one won't work, a so called **invalid** expression:
```
3+"ab"
```
> *Try it:* See what happens if you run these in your Python shell!

Notice how Python returns this error when you run the invalid expression example:
```
TypeError: unsupported operand type(s) for +: 'int' and 'str'
```
First of all:
> *Note:* Errors are **normal**, do not panic, as a programmer, you will generate **A LOT** of errors of all kinds.  

> *Note:* While writing your own code, or even when you type in code from this guide, you will at some point run into an error of some kind; make sure you **read** your error message! They are a programmer's ***BEST FRIENDS***

Let's look at the error Python threw when you entered the expression *3+"ab"*.  
Looks like something went wrong because you tried to mix datatypes: the first word "TypeError" is rather clear about this.  
It even explains that your *operands*, eg: the operand *3* and the operand *"ab"* cannot be used like you tried to with the operator *+*.

| error message | error explanation                | operator | operand A | operand B |
| :---          | :---                             | :---     | :---      | :---      |
| TypeError:    | unsupported operand types(s) for | +:       | 'int'     | 'str'     |

> *Note:* Notice how 'int' and 'str' are used instead of "integer" and "string"

## Statements
Statements are basically expressions chained together to do *something*.

So let's recap:

```
8
```
This is an *int*. It has the *value* 8.
```
3*5
```
This is an *expression*. It consists of the `\*` `operator` which does something to it's `operands`: `3` and `5`.
```python
print(3*5)
```
This is a very simple statement, it makes use of the print() function (more on that in a short bit) and you should be able to point out the *expression* `3*5`.

## Variables: defining and naming
Variables can be used to "refer to data". When you are just getting started with programming you could think of variables as boxes to put data in; the box has a name and when you want to get the info out of the box, you look up the right box by it's name, and then get the info out.

However, a better way to look at it, is this: variables are like an address on a street: a variable will tell you where certain data is; much like the address to a museum or bar will tell you where said place is. Simply put: variables point to values.

### Assignment
*Assign* data to a variable with `=`

So in it's most simple form use:
```
x = 8
```
`x`  now holds the *value* `8`.

Variables can have any name you want:
```
some_variable = 8001
```
Once the above code has run, you can quickly get out the data (9001) by referring to 'some\_variable' like in the following example:
```
print(x)
print(some_variable)
```

This should print the following into your terminal:
```
8
8001
```

### Type
Variables inherit type from the data they refer to.
```
x = 3
```

Will turn the *variable* `x` into an *int* (because `3` is an *int*)

You should keep in mind that, in Python, it's very easy to change the datatype of a variable:
```
x = "banana"
```
The same x that was an int before is now a string; operators that expect only ints will complain about this.
>Think about it: Could you imagine a situation where you would not want to have a variable that might hold both strings and ints?

### Usage
Wherever a value is used, a variable could take it's place. You will of course have to assign something to the variable somewhere, somehow.

For example, have a look at the following 2 examples. Notice the difference.
```
8 + 8
```
```
x = 8
x + x
```
>Consider this: Will the second example work if you remove the first line (`x = 8`)


### Variable names
#### Readability
Comments are one way to make code readable, another good tool is good variable names, lets say you are working with data that consists of just first and last names. You could do this:
```
x = Bob
y = Ross
```
Simply going with something such as in the following example will make working on and reading this code much easier.
```
first = Bob
last = Ross
```

#### Keywords
Some words in Python are so called keywords, this means that you cannot use them as variable names. A simple example of this would be `int`.
Your code editor or IDE will probably tell you that you are using a keyword by giving it a special color or showing some other form of warning.

## Data conversion
```
3+"ab"
```
The above expression won't work because the `+` operator cannot work with two different data types at the same time. The `3` is an int, `"ab"` is a string.

If you want to combine the int and the string you will have to change the integer `3` to a string: `"3"`.

### str()

The str() function lets us change the int 3 to a string "3"

The following code will work in Python:

```
str(3)+"ab"
```

### Caution

Be cautious when changing data types; changing data types somewhere in a large piece of code could easily lead to errors.

## Comments
### The 'hashtag' or 'pound'

Comments are lines (or blocks) of human readable text (so not code) that help you, or maybe others, to understand your code. 

Single line comments are defined with #, like this:
```
x = 1 #This is a comment
```

### Easy comment blocks
Multiline comments, or blocks are made by using:
```
'''
This is a multi line
comment
'''
```

### Where to comment
Since Python is meant to be an easy to read language and it is considered best practise to write understandable scripts, you will not have to put a comment on every little piece of code you write. Suppose you where to write this code:
```
my_answer = 3 + 3
```

This will set the variable my_answer to the value 6 (because 3+3 equals 6); you probably did not need this explanation to understand this line of code; so it would be futile to add a comment here.

The example below is a more complex example, note how it contains a comment that explains what this line of code does: 
```
line = re.sub(r"^\(|\)$|'|\s","",line) #remove all ( ) ' and whitespace from the string in the variable "line" using regular expressions.
```

### Disabling code
Instead of removing a line of code to test how a script works, lines can also be commented out, making it very simple to test with or without certain lines.

## Flow control: if, else and elif
### Branching; flow of control

You can now write code that runs from top to bottom: you can assign values and do calculations on them and then print them. However, to write more interesting code you want to be able to do tests. For example, you might want find out if a number is an even or an odd number.

To do this you can use conditionals:

### If / else

The basic form to use if (or other conditionals) is this:
```
if <some test>:
    block of instructions
else:
    block of instructions
```

Notice the indentation (the whitespace): the lines `if:` and `else:` are both to the most left part of the screen and end on a colon (`:`), the blocks of code that will be executed when the test (run on the line starting with `if`) returns a true, starts right after the `<some test>`: part, if the test returns a false, the first block will be skipped and the block of code after the else: will be run.

Indentation is extremely important in Python, it's how Python knows what blocks of code belong together: because the line that has `else:` on it starts to the far left again, the interpretor will know that the block of code that belongs to the if true statement has ended.

Let's say you want to find out if the variable n is an even number.

First you want to assign a value to n.
```
n = 5
```

Now, if you want to find out if n is an even number or not, you can use if to do something when n turns out to be even and another when n turns out to be an odd number.

In code this would look like this:

```
n = 5
if n%2 == 0:
    print("even")
else:
    print("odd")
```

An if doesn't require an else to function.

You can use if inside of a block of code that contain more ifs, this allows you to build more complicated branches.

### Comparing

Notice the == between n%2 and 0 in the code above. Remember how = is used to assign values to variables. This means that you need another way to tell the computer that you want to compare something. To tell the computer that you want to compare x to y you can use ==, like this:
```
if x == y:
    print("x is y!")
```

### Elif

Elif stands for else-if, Elif allows you to build much more complex expressions that can do tests that are run after tests, after tests, and so on.

The following example should easily explain how this works:

```
print("Guess the number! It's somewhere between 1 and 5! (Enter 1, 2, 3, 4 or 5 and press return!)")
n = input()
if n == 1:
    print("Super wrong!")
elif n == 2:
    print("Wrong!")
elif n == 3:
    print("Not bad!")
elif n == 4:
    print("Close!")
elif n == 5:
    print("Correct!")
else:
    print("Learn to read!")

```
## Loops: while
### Iteration / loops

### While

In a real world situations you often end up in situations that require us to do something while some test is true. A simple example:
```
While you are at work:
    wear pants
```
In programming you often want to have the machine do exactly this, let's look at a simple example in Python code:
```
name = ''
while name != 'your name':
    print('Please type your name.')
    name = input()
print('Thank you!')

```
The above program checks the user input and unless the input is equal to "your name", the script will begin from the start. If the check turns out to be true, the program will print a thank you and finally end. Be careful when writing loops; make sure there is a way to escape them, otherwise you will end up with an endless loop.

Example of an endless loop:

```python3
name = ''
banana = ''
while banana != 'your name':
    print('Please type your name.')
    name = input()
print('Thank you!')

```
## Input
The previous chapter's final example had you enter some text into the terminal. Python then stored the input in a variable.

Handeling input with the input function in Python is super simple.
```
x = input()
```
When this code runs, you can enter text into the terminal, whatever you type into the terminal (press enter when you are done), will be stored in the variable x.

Data that is entered through input() is always a string. So even if you enter
```
8
```
x =
```
'8'
```
and NOT:
```
8
```
## Imports
Importing modules is an important part of Python. Imports enable you to easily add extra functions to your script. A pretty obvious example is the 'os' module.

You can add the import module by adding the following to the top of your script:
```
import os
```

From there on you can use the functions from the os module by first typing
```
os
```
followed by a dot ('.') and the name of the function you want to use.

Let's say that you want to use the 'system' function from the os module. With 'system' you can send a bash command to the terminal. So for example, you could use:
```
os.system('ls')
```
This is effectively the same as typing
```
ls
```
into a terminal.

There are many modules enabling you to do all kind of different things. Python comes with a lot of modules you can import right away ('os' is one of them).

You can easily add more modules to use by installing them through pip.

## Test yourself
Write a new script for every exercise. Simply name your scripts after the module your are working on:
```
programming_intro_ex_0.py
programming_intro_ex_1.py
...
```
### Exercise 0: Define a variable
1. Write a script with a variable named 'x' and give it the value 309238423842039842398230948239048209348

### Exercise 1: Print it
1. Use your variable 'x' from the previous exercise.
2. Use Python's print function to print your variable's contents.

### Exercise 2: Greetings!
1. Print 'Hello, what is your name?'
2. Let the user enter their name.
3. Print 'Your name is *NAME*', where *NAME* should be the input entered in step 2.

### Exercise 3: The age old question
1. Print 'What is your age?'
2. Let the user enter a number (their age)
3. Print 'Your age is *AGE* where *AGE* should be the input from step 2.

### Exercise 4: Combo
1. Print 'Hello, please enter your name and age'
2. Let the user enter their name
3. Let the user enter their age
4. Print 'Your name is *NAME*, and you are *AGE* years old!'. Where *NAME* is the name from step 2 and *AGE* is the age from step 3.

### Exercise 5: Which one?
1. Print 'Do you prefer apples or bananas?'
2. Let the user enter an answer.
3. If the answer is 'apples, print 'you love apples!' otherwise, print 'you love bananas!'

### Exercise 6: Other!
1. Reuse the script from the previous exercise.
2. Change the first print to: 'Do you prefer apples, bananas or other?'
3. If the answer is 'apples, print 'you prefer apples!', if the answer is 'bananas, print 'you prefer bananas', otherwise print: 'you prefer something else!'

### Exercise 7: Wrong!
1. Reuse the script from the previous exercise.
2. Whenever the user enters an answer, test if the answer is either 'apples', 'bananas' or 'other'. If the answer is not one of those three, print 'That is not a valid answer! Answer again!' and let the user enter an answer again.
3. Keep asking until the user enters either 'apples', 'bananas' or 'other'.

### Exercise 8: Reading is important
1. Print 'Please enter "your name"'
2. Let the user answer something.
3. If the input is equal to 'your name', print 'thank you!' and stop, otherwise repeat the question.

### Exercise 9: A simple calculator
1. Print 'Please pick an operation: +/-'
2. Let the user enter '+' or '-'
3. Print 'Please enter your first number'
4. Let the user enter a number.
5. Print 'Please enter your second number'
6. Let the user enter a number.
7. Print 'You want to use *OPERATION* on *NUMBER1* and *NUMBER2*, the result is *RESULT*', where *OPERATION* is either '+' or '-', *NUMBER1* and *NUMBER2* are the numbers you entered in step 3 and 5 and result is the result of *NUMBER1* *OPERATION* *NUMBER2*.

### Exercise 10: Almost a full calculator
1. Use the calculator you wrote in the previous exercise.
2. Have your script complain and ask for a valid operation (so '+' *or* '-') whenever the user answers something other.

### Exercise 11: Finish it
1. Use the calculator from the previous two exercises.
2. Make sure your calculator can now also take the / (divide) and * (times) operators.
3. Add a comment line above every important step in your script.
4. Add a docstring (a '''Text goes here!''') at the very top of your script, describing in short what your script does.

### Bonus 1: Oneliner
1. Build your calculator script from the previous exercises in such a way that users can enter their entire calculation in one single line (so instead of going '+' **enter**, 8 **enter**, 2 **enter**, let your user type 8+2 **enter**).
2. Update comments to reflect changes you have made to your script.

## Further reading
If you want practical use cases for your new knowledge and or want to learn more about Python, consider having a look at these:

| Topic                | note | url                                          |
| ---                  | ---  | ---                                          |
| ATBS - ATBS Intro    |      | https://automatetheboringstuff.com/chapter0/ |
| ATBS - Python Basics |      | https://automatetheboringstuff.com/chapter1/ |
| Kaggle - Python class|      | https://www.kaggle.com/learn/python          |

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
