---
title: Redmond Python Meetup Onboarding
date: 2018-03-24 13:45:35
---

## Overview

Welcome!

If you are reading this page, you have expressed an interest in attending the Redmond Python Meetup. The Redmond Python Meetup is for *everyone*--from new programmers to experienced developers.

This page will walk you through the following:

- How to install Python on your computer
- How to use the Python Interpreter to run Python code
- How to write and manipulate basic Python data types, functions, and loops

At this point, you probably fall into one of three categories based on your experience level:

|Experience Level|Recommendation
|:---:|---|
|"I'm brand new to development and Python."|Come to the meetup for a guided on-boarding session with our TAs where you can complete this page and ask questions as you go. If you're feeling adventurous, you can start with installation below and try to get as far as you can.|
|"I'm new to Python but I have some programming experience."|Feel free to get as far as you can on this page and come to the meetup with questions, or you can come to the meetup and do an on-boarding session with our TAs.|
|"I'm an experience developer"|Feel free to go through this page on your own and come to the meetup with any questions|

## About Python

Python is an easy-to-write, easy-to-read interpreted scripting language. "Hello world!" is one line and looks like this:

```py
>>> print("Hello world!")
Hello world!
```
Here is a more complex example application that sends an email. It's still only 5 lines, though.

```py
import smtplib
server = smtplib.SMTP("smtp.gmail.com", 587)
server.login("youremailusername", "password")
msg = "/nHello!"
server.sendmail("you@gmail.com", "yourFriend@hotmail.com", msg)
```
The above code does the following:

1. Imports some code in an external module (code that we didn't write, but that are nevertheless using).
2. Creates an SMTP object to connect to a server.
3. Logs in to the server.
4. Creates our message.
5. Sends the message.

You don't need to understand this syntax at this time. The purpose of this example is simply to show you what you can accomplish in a few lines of Python code, which may take dozens of lines in other programming languages.

## Basic Python Features

There are a few characteristics of Python that you should remember:

- **Python is open source**: Anyone can see all of the underlying code and everyone has the chance to contribute to the code base.
- **Python is object-oriented**: Everything in Python is an object.
- **Python is platform-independent**: You can write an application on one operating system and run it on another.
- **Python has a minimalist design philosophy**: This emphasizes cleanliness and readability, with minimal semicolons and brackets.

## What kinds of things can you do with Python?

The sky is the limit, but here are some examples:

  - Interact with files on your computer
  - Automate tasks as part of a workflow
  - Scrape data off a website
  - Build and deploy REST APIs
  - Build games
  - Interact with cloud services (AWS, Azure, Google, etc.)

# Setup

## Installing Python

Let's first get Python installed on your computer. There are two major versions of Python out there in the wild right now: Python 2 and Python 3. Python 2 is retiring in 2020, so we'll be using Python 3.

In fact, you might already have one of these versions installed on your computer. Let's check:

1. Open a terminal or command prompt.
    - **WIN**: Start Menu > Command Prompt.
    - **MAC/LIN**: Application > Terminal.
2. Type `python` and hit **ENTER**. Do you see something like this? It means you have Python 3 installed on your computer.
    ```bash
    Python 3.6.4 (default, Jan  3 2018, 12:27:09)
    [GCC 4.2.1 Compatible Apple LLVM 9.0.0 (clang-900.0.39.2)] on darwin
    Type "help", "copyright", "credits" or "license" for more information.
    >>>
    ```
    If you get an error, you probably need to install Python. Note that you may have Python 2 installed (it will say `Python 2.x.x`), in which case you'll want to install Python 3.

See the following pages for platform-specific instructions on installing Python:

- [Windows](/setupwindows)
- [MacOS](/setupmac/)
- [Linux](/setuplinux/)

When you're finished, come back here and continue to the next section.

## Using the Python Interpreter

Now that we have Python installed, let's open the Python interpreter. The interpreter is a small application that let's us type some Python and execute it easily:

1. Open a terminal or command prompt like you did in the previous section.
2. Type `python` and hit **ENTER**.

Your prompt should look something like the following (if it doesn't, let a TA know):
```
Python 3.6.4 (default, Jan  3 2018, 12:27:09)
[GCC 4.2.1 Compatible Apple LLVM 9.0.0 (clang-900.0.39.2)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
```
You'll know you're in the Python interpreter when you see this prompt:
```
>>>
```
This means the Python interpreter is ready for your input. We can type Python code directly into this prompt and it will execute. Note that as you go through this on-boarding page, you'll see code samples like this:
```
>>> a = "Hello"
```
This means that you can type this line in at the `>>>` prompt. Simply enter the line of code, hit **Enter** after every line you enter, and note the output (although sometimes there won't be any!).

**Tip**: Don't copy and paste commands -- type them out. You'll learn far more if you take the time to type everything yourself.

To exit the interpreter:

1. Type `exit()` or hit `ctrl+d` to exit the Python interpreter and return to the computer's terminal.
2. Now, reopen the Python interpreter. A key point here is that everything that you entered in that previous Python interpreter session is **lost** between sessions. **The data does NOT persist**.

For now, we'll just be working with Python via the interpreter while we learn the basics. We'll show you later how to write lines of code in a file and run a full Python script at the command line.

# Getting Started with Python Code

## Basic Operations

Let's do some basic operations in Python to teach you how to interact with the Python interpreter.

1. Open the Python interpreter like we showed you in the previous section.
2. Type the following lines, noting the output:
  ```py
  >>> 2 + 4
  >>> 5 - 1
  >>> 3 * 4
  >>> 10 / 2
  ```
  Awesome! This is how easy it is to write and execute Python. This also introduces you to some basic math operations available to you in Python like addition, subtraction, etc. We'll expand on those later.

  Now try these:
  ```py
  >>> 2+4
  >>> 5-1
  >>> 3*4
  >>> 10/2
  ```
  Same operations as before. Note that the whitespace between values, in this case, doesn't matter. In Python, `2+4` is the same as `2 + 4`.

## Variables

Next, let's introduce variables. Variables are used to store values--numbers, words, lists of numbers and words, etc. This allows us to reference these variables later in our application. Imagine if you were writing an application and wanted to display your company name in 20 different places. Instead of writing your company name out 20 times, you can write it once and store it in a variable, and then reference the variable wherever you need it.

### Storing Numbers

Let's create a few variables that store some simple numbers. We'll use the `=` symbol to store values. This equals sign is formally called the **assignment operator**.
```py
>>> x = 4
>>> y = 2
>>> print(x + y)
```
What did we just do?

1. We assigned the number 4 to the variable "x" and the number 2 to "y".
2. We then called the "print" function to print the sum. `print()` is a built-in function that we can access anywhere, and always prints the contents out to the console.

For experienced developers, note that we don't have to tell the interpreter that our variables are numbers. We just assign and run. Python will assign the type automatically when we run our program ("at runtime").

## Storing Strings

Numbers are great, but let's try entering some strings of text. Go ahead and type the following, replacing the value for the `name` variable with your name below:
```py
>>> name = 'Your Name'
>>> print(name)
>>> fav_food = "Pasta"
>>> print(fav_food)
>>> long_multiline_string = """When in the Course of human events it becomes necessary for one people to dissolve the political bands which have connected them with another and to assume among the powers of the earth, the separate and equal station to which the Laws of Nature and of Nature's God entitle them, a decent respect to the opinions of mankind requires that they should declare the causes which impel them to the separation."""
>>> print(long_multiline_string)
```
Notice the use of quotes--single, double, or triple quotes are acceptable in Python. Just be consistent throughout your application! To keep things simple, we'll use double quotes and all of our variables will start with a lowercase letter for now. We'll be expanding on variables and functions later.

>*Remember*: Once you close the interpreter, all of this data is lost.

## Numbers

There are two number data types in Python 3:

- **integers**: Whole numbers with no decimal point (e.g. 1, 2, -504803, 6238746289374692837649283764829).
- **floats**: Written with a decimal point dividing the integer and fractional parts (e.g. .5, 842.32, .000238923).

Math in Python looks a lot like math with a calculator. Type the following into the interpreter.

### Addition

```py
>>> 2 + 2
>>> 1.65 + 2.15
>>> 2 + 1.65
```

### Subtraction

```py
>>> 12 - 5
>>> 45.9 - 25.3
>>> 2 - -4
```

### Multiplication

```py
>>> 6 * 7
>>> 5.6 * 4.3
>>> 6 * -5
```

### Division

```py
>>> 12/3
>>> 16/5
>>> 10/-5
```

If you’ve used Python 2, you’ll see that division works differently in Python 3. Python 2 uses floor division for integers, meaning it will return only the whole number part of the answer. Python 3 performs true division, returning the real or true value of the division. Try the following, one with one `/` and the other with two `//`:
```py
>>> 16/5
>>> 16//5
```

### Modulus

Thinking back to long division that you may have learned in school, the modulus is the “remainder” after performing division. It uses the % symbol.
```py
>>> 16%5
>>> 50%4
```

### Order of Operations

Order of operations works just like you learned in math class - Parentheses, Exponents, Multiplication, Division, Addition, Subtraction.
```py
>>> 5 + 4 * 3
>>> (5 + 4) * 3
```

> **Note:** We've just covered a lot! Using the interpreter, variables, entering basic data types, doing some basic math....questions? Ask a TA!

## Booleans

So far, the code we've written has been *unconditional*: no choice is getting made in the program--all of the code runs. Python has another data type called a **boolean** that is helpful when writing code that makes decisions. Booleans hold two values: `True` and `False`.

Open the Python interpreter and type these:
```py
>>> True
>>> type(True)
>>> False
>>> type(False)
>>> true
>>> false
```

### Testing for Equality

You can use booleans to test if Python objects are equal or unequal. The result is a boolean. Try typing these expressions in your Python console (note that the double equals tests for equality):

```py
>>> 0 == 0
>>> 1 == 0
>>> 54 = 42
```

Use `==` to test for equality. Recall that `=` is used for assignment of a variable to a value. This is an important idea and can be a source of bugs until you get used to it: `=` is assignment, `==` is comparison.

### Testing for Inequality

To test for inequality, use `!=`:

```py
>>> "a" != "a"
>>> "a" != "A"
```
The above example demonstrates an important point: Python is CASE-SENSITIVE. Uppercase and lowercase matter.

### Comparison Operators

Next, let's look at comparison operators. `<`, `<=`, `>`, and `>=` have the same meaning as in math class. The result of these tests is a boolean:

```py
>>> 1 > 0
>>> 2 >= 3
>>> -1 < 0
>>> .5 <= 1
```

### Membership Operators

Finally, let's briefly look at membership operators. You can check for membership using the `in` keyword, which also results in a boolean:
```py
>>> "H" in "Hello"
>>> "h" in "Hello"
>>> x = "He"
>>> x in "Hello"
```
Or check for a lack of membership with `not in`:
```py
>>> "a" not in "abcde"
>>> "Chicago" not in "Redmond Python Workshop"
```

## Operators

We just introduced some operators that let us further manipulate our data. We've outlined some (not all) of the Python operators in the following tables:

### Assignment Operators

|Operator|Description|Example|
|:----:|---|---|
|`=`|Assigns values from right side operands to left side operand|`c = a + b` assigns value of `a + b` into `c`|
|`+=` Add AND |Adds right operand to the left operand and assign the result to left operand|`c += a` is equivalent to `c = c + a`|
|`-=` Subtract AND|Subtracts right operand from the left operand and assign the result to left operand|`c -= a` is equivalent to `c = c - a`|
|`*=` Multiply AND|Multiplies right operand with the left operand and assign the result to left operand|`c *= a` is equivalent to `c = c * a`|
|`/=` Divide AND|Divides left operand with the right operand and assign the result to left operand|`c /= a`  is equivalent to `c = c / a`|
|`%=` Modulus AND|Calculates modulus using two operands and assign the result to left operand|`c %= a` is equivalent to `c = c % a`|
|`**=` Exponent AND|Performs exponential calculation on operators and assign value to the left operand|`c **= a` is equivalent to `c = c ** a`|
|`//=` Floor Division|Performs floor division on operators and assign value to the left operand |`c //= a` is equivalent to `c = c // a`|

Exercise:
```py
>>> a = 21
>>> b = 10
>>> c = 0
>>> c = a + b
>>> c
>>> c += a
>>> c
>>> c *= a
>>> c
>>> c /= a
>>> c
>>> c = 2
>>> c %= a
>>> c
>>> c **= a
>>> c
>>> c //= a
>>> c
```

### Comparison Operators

Assume `a = 5` and `b = 10`.

|Operator|Description|Example|
|:---:|---|---|
|`==`|If the values of two operands are equal, then the condition becomes true.|`a == b` evaluates to false.|
|`!=`|If values of two operands are not equal, then condition becomes true.|`a != b` is true.|
|`>`|If the value of left operand is greater than the value of right operand, then condition becomes true.|`a > b` is not true.|
|`<`|If the value of left operand is less than the value of right operand, then condition becomes true.|`a < b` is true.|
|`>=`|If the value of left operand is greater than or equal to the value of right operand, then condition becomes true.|`a >= b` is not true.|
|`<=`|If the value of left operand is less than or equal to the value of right operand, then condition becomes true.|`a <= b` is true.|

Exercise:
```py
>>> a = 5
>>> b = 10
>>> a == b
>>> a != b
>>> b = 5
>>> a == b
>>> a != b
```

**Key Point**: `=` assigns a value, `==` tests for equality, `!=` tests for inequality.

### Logical Operators

|Operator|Description|Example|
|:---:|---|---|
|`and`|If both the operands are true then condition becomes true.|`x>4 and y<5`|
|`or`|If any of the two operands are non-zero then condition becomes true.|`x>4 or y<5`|
|`not`|Used to reverse the logical state of its operand.|`not(x and y)`|

### Identity Operators

|Operator|Description|Example|
|:---:|---|---|
|`is`|Evaluates to true if the variables on either side of the operator point to the same object.|See below.|
|`is not`|Evaluates to false if the variables on either side of the operator point to the same object.|See below.|

Exercise:
```py
>>> a = 1
>>> b = 1
>>> a is b
>>> b = 2
>>> a is b
```

## Conditional Branching

### Using `if`

Now that we know how to check if something is `True` or `False` using booleans and operators, we can use "conditional branching" to make Python execute commands on a conditional basis. Just take a look at the following code:

```py
if 6 > 5:
     print("Six is greater than five!")
```

This is the first piece of Python we've written that crosses multiple lines, and the way to enter it at a Python interpreter's prompt is a little different than single lines of code.

In the interpreter:

1. Type `if 6 > 5:`, and hit `ENTER`. The next line will have `...` as a prompt, instead of the usual `>>>`. This is Python telling us that we are in the middle of a code block, and so long as we indent our code it should be a part of this code block.
2. Type 4 spaces, type `print("Six is greater than five!")`, and then hit `ENTER` to end the line. Note that spaces are [officially the preferred indentation method](https://www.python.org/dev/peps/pep-0008/#tabs-or-spaces).
3. Finally, hit `ENTER` again to tell Python you are done with this code block. All together, it will look like this:

```py
>>> if 6 > 5:
...      print("Six is greater than five!")
Six is greater than five!
```

So what's going on here? When Python encounters the `if` keyword, it evaluates the expression following the keyword and before the colon.

  - If that expression evaluates to `True`, Python executes the code in the indented code block under the `if` line.
  - If that expression evaluates to `False`, Python skips over the code block.

In this case, because "6 is greater than 5" evaluates to true, Python executes the code block under the if statement, and we see "Six is greater than five!" printed to the screen. Guess what will happen with these other expressions, then type them out and see if your guess was correct:

```py
>>> if 0 > 2:
...     print("Zero is greater than two!")
```
Another:
```py
>>> if "banana" in "bananarama":
...    print("I miss the 80s.")
```
One more:
```py
>>> if "Ringo" not in "John, Paul, and George":
...    print("Ringo wasn't much of a songwriter.")
```

### Using `if` and `else`

You can use the `else` keyword to execute code only when the `if` expression isn't `True`:

```py
>>> sister_age = 15
>>> brother_age = 12
>>> if sister_age > brother_age:
...    print("sister is older")
... else:
...    print("brother is older")
```

Like with `if`, the code block under the `else` statement must be indented so Python knows that it is a part of the `else` block.

### Using `and` and `or`

We've been testing single conditions, but we can also test multiple conditions that result in execution of some code. You can check multiple expressions together using the `and` and `or` logical operators.

- If two expressions are joined by an `and`, they **both** have to be `True` for the overall expression to be `True`.
- If two expressions are joined by an `or`, as long as **at least one** is `True`, the overall expression is `True`.

Try typing these out and see what you get:

```py
>>> 1 > 0 and 1 < 2
>>> 1 < 2 and "x" in "abc"
>>> "a" in "hello" or "e" in "hello"
>>> 1 <= 0 or "a" not in "abc"
```
Guess what will happen when you enter these next two examples, and then type them out and see if you are correct. If you have trouble with the indenting, call over a staff member and practice together. It is important to be comfortable with indenting. Indenting is a crucial part of the syntax of Python.

```py
>>> temperature = 32
>>> if temperature > 60 and temperature < 75:
...    print("It's nice and cozy in here!")
... else:
....    print("Too extreme for me.")
```
One more:
```py
>>> hour = 11
>>> if hour < 7 or hour > 23:
...    print("Go away!")
...    print("I'm sleeping!")
... else:
...    print("Welcome to the cheese shop!")
...    print("Can I interest you in some choice gouda?")
```

You can have as many lines of code as you want in if-else block, just make sure to indent them so Python knows they are a part of the same indentation block.

### Using `elif` and `else`

If you have more than two cases, you can use the `elif` keyword to check more cases. Think of `elif` as Python-speak for else if. You can have as many `elif` cases as you want. Python will go down the code checking each `elif` until it finds a `True` condition or reaches the default `else` block.

```py
>>> sister_age = 15
>>> brother_age = 12
>>> if sister_age > brother_age:
...    print("sister is older")
... elif sister_age == brother_age:
...    print("sister and brother are the same age")
... else:
...    print("brother is older")
```

You don't have to have an `else` block if you don't need it. That just means there isn't default code to execute when none of the `if` or `elif`conditions are `True`:

```py
>>> color = "orange"
... if color == "green" or color == "red":
...    print("Christmas color!")
... elif color == "black" or color == "orange":
...    print("Halloween color!")
... elif color == "pink":
...    print("Valentine's Day color!")
```

If `color` had been "purple", the code wouldn't have printed anything. Remember that `=` is for assignment and `==` is for comparison.

## Functions

Functions are how we perform actions on our data. We've been using a function a lot so far: `print()`. Calling a function is as easy as calling the function name and putting a variable or value between round brackets like we've been doing.

Try the following:
```py
>>> a = "The number 3: "
>>> b = 3
>>> type(a)
>>> type(b)
>>> print(a, b)
```

The values between the `()` brackets are called "arguments." Certain functions let us pass arguments to our functions. like so:
```py
>>> str1 = "Bill is"
>>> a = 50
>>> str2 = "years old."
>>> print(str1, a, str2)
```
There are three basic categories of functions:

- The built-in kind that come with Python when we install it (e.g.`print()`)
- The kind we write ourselves
- The kind that other people wrote that we can borrow (by importing their code modules and using them in our programs)

We've already introduced the built-in kind. Next, we'll show you how to write your own. Later, we'll show you how to import and use functions written by other people.

### Writing Our Own Function

In the interpreter, write the following code:
```py
>>> def myFirstFunction():
...     print("Hello!")
```
We just wrote our first function! Now call it:
```py
>>> myFirstFunction()
```
Our function takes no arguments. Let's write a function that passes an argument:
```py
>>> def mySecondFunction(name):
...     print("Hello", name)
```
Now let's run it, passing in the name of your choice:
```py
>>> mySecondFunction("Bill Gates")
```
Fantastic! You just authored and called your first function that passed an argument.

### Utility Functions

We'll gradually expand your knowledge of functions, but for now we'll introduce a few other built-in functions that can help us with numerical types and strings.

#### For Numbers

We can convert between numerical types with ease.

Convert from float to int:
```py
>>> x = 5.5
>>> x
>>> type(x)
>>> x = int(x)
>>> x
>>> type(x)
```
Convert from int to float:
```py
>>> y = 4
>>> y
>>> type(y)
>>> y = float(y)
>>> y
>>> type(y)
```
#### For Strings

`upper()` and `lower()` are handy:
```py
>>> str = "My String"
>>> str.upper()
>>> str.lower()
```

## Additional Concepts

Let's briefly introduce some additional concepts and tools that will help you on your journey with Python.

### Tracebacks

When you make a mistake and try to run your program, Python will generate a traceback to tell you what went wrong. By now, you may have seen a few of these!

Open the interpreter and run:
```py
>>> a = "John"
>>> a + 2
```
We see the following error:
```py
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: must be str, not int
```
The above traceback tells us the following:

- The name of the file where the error occurred: "<stdin>" (means that the error occurred on input)
- The line number containing the error: 1
- The name of the module (if applicable, which it's not here)
- The error type: `TypeError`
- What we did wrong: We tried to perform an operation on one data type that Python wouldn't allow.

Tracebacks are invaluable when trying to diagnose why something won't run.

### Comments

Comments help us communicate with teammates about what our functions are doing. We'll use them more when we start running applications in Python files. For now, just know that when you see the following syntax, it's a comment. There's no need to enter the code below, just familiarize yourself with the concepts.

Single line comment:
```py
# Here is a comment in python! It's great and is ignored when the program runs!
name = "Your Name"
print(name)
print("Your Name")
```
This is an in-line comment:
```py
name = "Your Name"
print(name) # Here is an in-line comment!
print("Your Name")
```
Here is a multiline comment that uses three apostrophes above and below the comment:
```py
'''
This is a multiline comment for longer comments that you want to put in your code. Commenting code is important when you're sharing code with multiple people. Because we're using the three apostrophes, we can make this comment as looooooooooong as we want!
'''
name = "Your Name"
print(name)
print("Your Name")
```

# Wrap-up

We just covered a LOT of material. Remember:

1. We've just barely scratched the surface here. We have have skipped some things. That's ok! This is supposed to be an introduction. Over time, you will fill in the gaps.
2. If something is unclear, **ask for help**. That's why we're here.
3. If you don't understand something or feel overwhelmed, **keep at it**. This is just the beginning of a long journey towards learning the ins and outs of Python.

## Additional Resources

There is no shortage of additional resources on Python. It helps to read multiple articles and tutorials on the core concepts mentioned above, so we encourage you to read and explore the following:

- [Python Guide for Beginners - Non-Programmers](https://wiki.python.org/moin/BeginnersGuide/NonProgrammers)
- [Python Guide for Beginners - Programmers](https://wiki.python.org/moin/BeginnersGuide/Programmers)

### Coding Exercises

- [Coding Bat](https://www.codingbat.com/python)
- [Hacker Rank](https://hackerrank.com)

### Other Tools

- [Try Git](https://www.codeschool.com/courses/try-git)
