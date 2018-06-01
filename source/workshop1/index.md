---
title: Workshop - Part 1
date: 2018-03-24 18:42:48
---

This is the self-guided, self-paced tutorial for part 1. We've included a break in the middle, but remember to take a break to stretch, get some water, or take a moment to relax any time you need to. If at any time you have questions, ask away!

If you've not yet done so, ensure you've gone through [these setup instructions](/setup) to install and configure Python.

## Using This Tutorial

As you go through this tutorial, you'll see code samples like this:

`a = "Hello"`

This means that you can type this line in at the `>>>` prompt in your Python shell. Simply enter the line, hit **Return** or **Enter** after every line you enter, and note the output (although sometimes there won't be any!). 

**Tip**: Don't copy and paste commands -- type them out. You'll learn far more if you take the time to type everything yourself.

### Math

Math in Python looks a lot like math with a calculator.

#### Addition

```py
2 + 2
1.65 + 2.15
2 + 1.65`
```

#### Subtraction

```py
12 - 5
45.9 - 25.3
2 - -4
```
#### Multiplication

Multiplication uses the `*` (asterisk or star) symbol.

```py
6 * 7
5.6 * 4.3
6 * -5
```

#### Division

Division uses the `/` symbol.
```py
12/3
16/5
10/-5
```
**Note**: If you've used Python 2, you'll see that division works differently in Python 3. Python 2 uses floor division for integers, meaning it will return only the whole number part of the answer. Python 3 performs true division, returning the real or true value of the division.

To get *only* the whole number in Python 3, use this syntax:
```py
16//5
50//4
```
#### Modulus

Thinking back to long division that you may have learned in school, the modulus is the "remainder" after perfoming division.  It uses the `%` symbol.
```py
16%5
50%4
```
#### Order of Operations

Order of operations works just like you learned in math class - Parentheses, Exponents, Multiplication, Division, Addition, Subtraction.

```py
5 + 4 * 3
(5 + 4) * 3
```
### Types

There's a helpful function (more on what a function is later) called `type` that tells you the data type of a given variable. We can check for ourselves that Python considers '1' and '1.0' to be different data types:

```py
type(1)
type(1.0)
```
So now we've seen two data types: *integers* and *floats*. We'll see more data types as we work through the lesson.

We also used the term "function" without explaining what it is -- we'll talk about functions more in a bit, and write our own, but for now know these things:

* Functions encapsulate some useful bit of work. We save that useful bit of work inside a function so we don't have to type it repeatedly. For example, some nice person decided that being able to determine the type of an object was useful, so he or she put the Python code that figures out an object's type into the function `type()`, and now we all get to use it, instead of having to write it ourselves.
* Functions are sort of like functions in math class. You can provide input to a function and it produces output. The `type()` function takes data as an input, and produces what type of data the data is (e.g. an integer or a float) as output.
* To use a function, write the name of the function followed by an open parenthesis, what the function takes as input (we call that input the arguments to the function), and then a close parenthesis.

So in our case, 'type' is the name of the function, and it takes one argument; in the two examples above, we first give type an argument of 1 and then give it an argument of 1.0.

---
**Stop for a moment here and try pressing the up arrow on your keyboard a few times. The Python interpreter saves a history of what you've entered, so you can arrow up to old commands and hit Return to re-run them -- just like your computer's command prompt!**

---

### Variables

A lot of work gets done in Python using variables. A variable consists of an identifier (the variable's name) and a value stored in the variable -- any kind of value, not just a number. In the example below, `x` is our identifier and `4` is the value stored:
```py
type(4)
x = 4
x
type(x)
2 * x
```
Giving a name to something so that you can refer to it by that name later is called assignment. Above, we assigned the name 'x' to 4, and after that we can use x wherever we want to use the number 4.

The space between the identifier, the equal sign, and its value does not matter. The two variables below are indentical. However, you should be consistent in your code.

x = 5
x=5

Variables can also be re-assigned.
```py
x = 3
x
x = 7
x
```
Be careful when you do this though... accidentally re-assigning a variable can cause bugs in your code. 

A variable's identifier can contain letters, numbers, and underscores. However, identifiers **must** start with a letter and can not contain any other special characters. Here are some valid variable names:
```py
magic_number = 1500
amountOfFlour = .75
my_name = "Jessica"
```
Projects develop naming conventions, so multi-word identifiers may use underscores (like `magic_number`), or "camel case" (like `amountOfFlour`). The most important thing is to **be consistent** within a project, because it makes the code more readable.

### Strings

So far we've seen two data types: *integers* and *floats*. Another useful data type is a *string*, which is just what Python calls a bunch of characters (like numbers, letters, whitespace, and punctuation) put together between quotation marks:
```py
"Hello"
"Python, I'm your #1 fan!"
```
Like with the numeric data types, we can check the type of a string:
```py
type("Hello")
type(1)
type("1")
```
You can assign a string value to a variable:
```py
my_car = "Toyota"
```
#### String Concatenation

You can concatenate (join) strings together using the `+` sign:
```py
"Hello" + "World"
"I drive a " + my_car
```
You can not concatenate a string with another data type.
```py
"Hello" + 123
```
will give you a *traceback*:

```
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: Can't convert 'int' object to str implicitly
```

A traceback provides details on what was happening when Python encounters an Exception or Error -- something it doesn't know how to handle. There are many kinds of Python errors, each with descriptive names to help us humans understand what went wrong. In this case we are getting a `TypeError`: we tried to do some operation on a data type that isn't supported for that data type.

Python gives us a helpful error message as part of the `TypeError`:

`"cannot concatenate 'str' and 'int' objects"`.

We can, however, use the `str()` function to convert a number to a string. Like the `type()` function we've been using, `str()` takes one argument as input and outputs it as a string.
```py
str(4)
str(5.34)
str("Ice cream")
```
#### String Length

There's another useful function that works on strings called `len()`. This returns the length of a string as an integer.
```py
len("Hello")
len("")
president = "Obama"
len(president)
```
#### Quotes

We've been using double quotes around your strings, but either double or single quotes are valid in Python:
```py
'Hello world'
"Hello world"
```
You do have to be careful about using quotes inside strings:
```py
'Let's learn Python together!'
```
will give you another `traceback`, for a `SyntaxError`. When Python evaluates this expression, it starts at the first single quote as the start of the string, and to the next single quote as the end of the string. Then it doesn't know what to do with the rest of the stuff that follows.

There are a few ways to solve this problem. One is to use double quotes on the outside:
```py
"Let's learn Python together!"
```
or we can *escape* the quote with a backslash:
```py
'Let\'s learn Python together!'
```
The backslash is a special character that tells Python to treat the next character literally, not as part of the syntax or code. Thus, you can do things like this:
```py
str = "Fernando said, \"Python is fun!\""
print(str)
```
#### Exercises

Let's take a look at a couple of exercises. Read the following lines of code, but don't execute them. Try to figure out what they will do. Sketch them out with pen and paper if you need to. Then type them in your terminal and execute them to see what happens.

1.

```py
total = 1.5 - 1/2 + ((-2.0/2) - (1.0/2))
print(total)
type(total)
```

2.

```py
a = "quick"
b = "brown"
c = "fox jumps over the lazy dog"
print("The " +  a * 3 + " " +  b * 3 + " " + c)
```

3.

```py
print(2.0 * 123 + str(2.0) * 123)
```

---
**Pause**: Let's take a break.  We've covered a lot!

---

#### Comments and New Lines

Below is an example of how to use comments and insert new lines:

```py
# The pound sign is used as a comment character in Python. Programmers
# use comments to annotate code. Python ignores everything after the
# comment character on a line.

# Notice how the 'print' command has been inserting a new line at the
# end of our strings.
print("The last three mayors of Philadelphia were:")

# We can insert newlines ourselves, using "\n".
print("Michael Nutter\nJohn Street\nEd Rendell")

# "" Is the empty string. Since the print command will insert a
# newline at the end, this will print a newline by itself:
print("")

# Here's a new kind of printing: you can use triple quotes to create
# multiline strings.
print("""Jim Kenney was elected Mayor
of Philadelphia on November 3, 2015, beating
Republican challenger Melissa Murray Bailey.""")

print("")

# When you use triple quotes, whitespace is preserved.
print("""Jim Kenney received
    84% of the
        popular vote""")
```

### Python Scripts

So far, we've been running code directly from the shell interpreter (the `>>>` prompt). This is great for testing and exploring short bits of code, but for longer projects we want to save our script in a file and run it from our computer's terminal. 

1. Copy and paste the entire code block from the previous section (including the comments) into a new text file and save it as `mayors.py`. Note the `.py` file extension, indicating that this is a Python script.
2. Open your computer's terminal (not the Python shell) and navigate to the directory where you saved this file. At your computer's command prompt, type:

  `python3 mayors.py`

  to run this script. Study what happens. Edit this file so it displays the last four mayors of Philadelphia (Look it up on [Wikipedia](https://en.wikipedia.org/wiki/List_of_mayors_of_Philadelphia) if you need to!). Save it and run it again.

**CHECKPOINT: Do you know how to do these things?**

: How do you run a Python script from your computer's terminal?
: How do you comment code in Python?
: How do you print just a newline?
: How do you print a multi-line string so that whitespace is preserved?

#### Booleans

So far, the code we've written has been *unconditional*: no choice is getting made--all of the code runs. Python has another data type called a **boolean** that is helpful for writing code that makes decisions. Booleans hold two values: `True` and `False`.

Re-open the Python console and try typing these:
```py
True
type(True)
False
type(False)
true
false
```
You can test if Python objects are equal or unequal. The result is a boolean. Try typing these expressions in your Python console:
```py
0 == 0
1 == 0
54 = 42
```
Use `==` to test for equality. Recall that `=` is used for assignment of a variable to a value. This is an important idea and can be a source of bugs until you get used to it: `=` is assignment, `==` is comparison.

Use `!=` to test for inequality:
```py
"a" != "a"
"a" != "A"
```
`<`, `<=`, `>`, and `>=` have the same meaning as in math class. The result of these tests is a boolean:
```py
1 > 0
2 >= 3
-1 < 0
.5 <= 1
```
You can check for containment with the `in` keyword, which also results in a boolean:
```py
"H" in "Hello"
"X" in "Hello"
```
Or check for a lack of containment with `not in`:
```py
"a" not in "abcde"
"Chicago" not in "Philadelphia Python Workshop"
```
#### Flow Control

Now that we know how to check if something is `True` or `False`, we can use this to make Python execute commands conditionally.

```py
if 6 > 5:
     print("Six is greater than five!")
```

That was our first multi-line piece of code, and the way to enter it at a Python prompt is a little different. 

1. First, type the `if 6 > 5:` part, and hit `enter`. The next line will have `...` as a prompt, instead of the usual `>>>`. This is Python telling us that we are in the middle of a code block, and so long as we indent our code it should be a part of this code block.
2. Type 4 spaces, type `print("Six is greater than five!")`, and then hit `enter` to end the line. 
3. Finally, hit `enter` again to tell Python you are done with this code block. All together, it will look like this:

```py
>>> if 6 > 5:
...      print("Six is greater than five!")
Six is greater than five!
```

So what's going on here? When Python encounters the `if` keyword, it evaluates the expression following the keyword and before the colon. If that expression is `True`, Python executes the code in the indented code block under the `if` line. If that expression is `False`, Python skips over the code block.

In this case, because 6 really is greater than 5, Python executes the code block under the if statement, and we see "Six is greater than five!" printed to the screen. Guess what will happen with these other expressions, then type them out and see if your guess was correct:

```py
if 0 > 2:
     print("Zero is greater than two!")
```

```py
if "banana" in "bananarama":
    print("I miss the 80s.")
```

**more choices: if and else**

You can use the `else` keyword to execute code only when the `if` expression isn't `True`:

```py
sister_age = 15
brother_age = 12
if sister_age > brother_age:
    print("sister is older")
else:
    print("brother is older")
```

Like with `if`, the code block under the `else` statement must be indented so Python knows that it is a part of the `else` block.

**compound conditionals: `and` and `or`**

We've been testing single conditions, but we can also test multiple conditions that result in execution of some code. You can check multiple expressions together using the `and` and `or` keywords. 

- If two expressions are joined by an `and`, they both have to be `True` for the overall expression to be `True`. 
- If two expressions are joined by an `or`, as long as at least one is `True`, the overall expression is `True`.

Try typing these out and see what you get:
```py
1 > 0 and 1 < 2
1 < 2 and "x" in "abc"
"a" in "hello" or "e" in "hello"
1 <= 0 or "a" not in "abc"
```
Guess what will happen when you enter these next two examples, and then type them out and see if you are correct. If you have trouble with the indenting, call over a staff member and practice together. It is important to be comfortable with indenting for tomorrow. Indenting is a crucial part of the syntax of Python.

```py
temperature = 32
if temperature > 60 and temperature < 75:
    print("It's nice and cozy in here!")
else:
    print("Too extreme for me.")
```

```py
hour = 11
if hour < 7 or hour > 23:
    print("Go away!")
    print("I'm sleeping!")
else:
    print("Welcome to the cheese shop!")
    print("Can I interest you in some choice gouda?")
```

You can have as many lines of code as you want in if and else block; just make sure to indent them so Python knows they are a part of the block.

**even more choices: elif and else**

If you have more than two cases, you can use the `elif` keyword to check more cases. Think of `elif` as Python-speak for else if. You can have as many `elif` cases as you want. Python will go down the code checking each `elif` until it finds a `True` condition or reaches the default `else` block.

```py
sister_age = 15
brother_age = 12
if sister_age > brother_age:
    print("sister is older")
elif sister_age == brother_age:
    print("sister and brother are the same age")
else:
    print("brother is older")
```

You don't have to have an `else` block if you don't need it. That just means there isn't default code to execute when none of the `if` or `elif`conditions are `True`:

```py
color = "orange"
if color == "green" or color == "red":
  print("Christmas color!")
elif color == "black" or color == "orange":
  print("Halloween color!")
elif color == "pink":
  print("Valentine's Day color!")
```

If color had been "purple", that code wouldn't have printed anything.

*Remember that `=` is for assignment and `==` is for comparison.*

#### Functions

Functions take input from the user or the application and (usually) produce output (e.g. they return a value). You can then assign a variable to this output. As we've shown in previous sections, you call a function by using its name followed by its arguments in parenthesis.

Why are functions important?

* They allow tasks to be run quickly and to be automated, i.e. they do some useful bit of work.
* They let us re-use code without having to type it out each time.
* They facilitate consistency and reduce the risk of error. 

Python has many built in functions. For example:

`length = len("Mississippi")`

Executing this code assigns the length of the string "Mississippi" to the variable length. We can write our own functions to encapsulate bits of useful work so we can reuse them. Here's how you do it:

**Step 1: Write a Function signature**

A function signature tells you how the function will be called. It starts with the keyword `def`, which tells Python that you are defining a function. Then comes a space, the name of your function, an open parenthesis, the comma-separated input parameters for your function, a close parenthesis, and a colon. 

Here's what a function signature looks like for a function that takes no arguments:

```py
def myFunction():
    # Your code would go here!
```

Here's what a function signature looks like for a function that takes one argument called my_string:

`def myFunction(my_string):`

And one for a function that takes two arguments:

`def myFunction(myList, myInteger):`

Parameters should have names that usefully describe what they are used for in the function. 

>Note: We've used the words parameters and arguments seemingly interchangeably to reference the input to functions. The distinction isn't really important right now, but if you're curious: in function signatures the input is called parameters, and when you are calling the function the input is called arguments.

**Step 2: Do useful work inside the function**

Underneath the function signature is where you do your useful work. Everything inside the function is indented, just like with if/else blocks, so Python knows that it is a part of the function. You can use the variables passed into the function as parameters, just like you can use variables once you define them outside of functions.

```py
def add(x, y):
    result = x + y
```

**Step 3: Return something**

If you want to be able to assign a variable to the output of a function, the function has to return that output using the `return` keyword.

```py
def add(x, y):
    result = x + y
    return result
```

or, even shorter:
```py
def add(x, y):
    return x + y
```

You can return any Python object: numbers, strings, booleans ... even other functions! Once you execute a return, you are done with the function -- you don't get to do any more work. That means that if you have a function like this:

```py
def absoluteValue(number):
    if number < 0:
        return number * -1
    return number
```

If `number` is less than 0, you return number * -1 and never even get to the last line of the function. However, if number is greater than or equal to 0, the if expression evaluates to False, so we skip the code in the if block and return number.

We could have written the above function like this if we wanted. It's the same logic, just more typing:

```py
def absoluteValue(number):
    if number < 0:
        return number * -1
    else:
        return number
```

**Step 4: Use the function**

Once you define a function you can use it as many times as you want. You can assign the value it returns to other variables and use those variables in other commands.

```py
def add(x, y):
    return x + y
```

```py
result1 = add(1234, 5678)
print(result1)
result2 = add(-1.5, .5)
print(result2)
print("The total sum is", result1 + result2)
```

Functions don't have to return anything if you don't want them to. They usually return something because we usually want to be able to assign variables to their output. If your function does not return anything, you won't be able to assign a variable to its output and won't be able to use its output anywhere else.

What do you think will happen here? Try it and see:

```py
def half_number(x):
    print(x/2)

half1 = half_number(20)
print(half1)
```

That's it for part 1! Now you can take some time to try some of the [practice exercises](/practice/) and review anything here that seemed challenging. We'll review all this and get deeper into Python during part two's presentation.

# [**Continue to Workshop: Part Two **](/workshop2)