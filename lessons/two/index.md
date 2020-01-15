**Table of Contents**

- [Variables](#Variables)
  - [Naming Rules](#naming-rules)
  - [NameError](#nameerror)
  - [More on Variables](#more-on-variables)
  - [Variables Problems](#variables-problems)
- [Strings](#strings)
  - [Single and Double Quotes](#single-and-double-quotes)
  - [Changing Case](#changing-case)
  - [Combining Strings](#combining-strings)
  - [Whitespace](#whitespace)
  - [Strings Further Reading](#strings-further-reading)
  - [Strings Problems](#strings-problems)

# Variables

A variable holds a value. The value can be a character, string, number, or boolean. More about these data types in future lessons.

**input**

```python
message = "Hello Python world!"
print (message)
```

**output**

```bash
$ Hello Python world!
```

A variable's value, like the name implies, can also change throughout a program.

**input**

```python
message = "Hello Python world!"
print (message)

message = "Python is my favorite language!"
print (message)
```

**output**

```
$ Hello Python world!
$ Python is my favorite language!
```

In the example above `message` prints two different values. Something to remeber is that computers read code like we do, from left to right, top to bottom.

## Naming Rules

1. Variables can **only** contain letters, numbers, and underscores. Variable names can start with a letter or an underscore, but can **not** start with a number.
2. Spaces are **not** allowed in variable names, so we use underscores instead of spaces. For example, use `student_name` instead of `student name`.
3. You cannot use [Python keywords](https://docs.python.org/2.5/ref/keywords.html) as variable names.
4. Variable names should be descriptive, without being too long. For example `mc_wheels` is better than just `wheels`, and `number_of_wheels_on_a_motorycle`.
5. Be careful about using the lowercase letter l and the uppercase letter O in places where they could be confused with the numbers 1 and 0.

## NameError

There is one common error when using variables, that you will almost certainly encounter at some point. Take a look at this code, and see if you can figure out why it causes an error.

**input**

```python
message = "Thank you for sharing Python with the world, Guido!"
print (mesage)
```

**output**

```
NameError                                 Traceback (most recent call last)
/home/ehmatthes/development_resources/project_notes/intro_programming/notebooks/<ipython-input-12-7966723379c3> in <module>()
      1 message = "Thank you for sharing Python with the world, Guido!"
----> 2 print(mesage)

NameError: name 'mesage' is not defined
```

Look at the error message and let's look through it. First, we see it is a `NameError`. Then we see the file that caused the error, and an arrow shows us what line in that file caused the error. Then we get some more specific feedback, that `name 'mesage' is not defined`.

You may have already spotted the source of the error. We spelled message two different ways. Python does not care whether we use the variable name `message` or `mesage`. Python only cares that the spellings of our variable names match every time we use them.

This is pretty important, because it allows us to have a variable `name` with a single name in it, and then another variable `names` with a bunch of names in it.

We can fix NameErrors by making sure all of our variable names are spelled consistently.

**input**

```python
message = "Thank you for sharing Python with the world, Guido!"
print (message)
```

**output**

```
$ Thank you for sharing Python with the world, Guido!
```

In case you didn't know [Guido van Rossum](https://en.wikipedia.org/wiki/Guido_van_Rossum) created the Python language over 20 years ago, and he is considered Python's Benevolent Dictator for Life. Guido still signs off on all major changes to the core Python language.

## More on Variables

...

## Variable Problems

1. [My Own Variable](#)

   Using what you've just learned, you'll create your own variable with custom message.
   
1. [One Variable, Two Messages](#)

   In this short problem you'll write one variable that stores two different messages.

# Strings

Strings are sets of characters. Strings are easier to understand by looking at some examples.

## Single and double quotes

- Strings are contained by either single or double quotes.

  ```python
  my_string = "This is a double-quoted string."
  my_string = 'This is a single-quoted string.'
  ```

- This lets us make strings that contain quotations.

  ```python
  quote = "Linus Torvalds once said, 'Any program is only as good as it is useful.'"
  ```

## Changing case

- You can easily change the case of a string, to present it the way you want it to look.

- It is often good to store data in lower case, and then change the case as you want to for presentation. This catches some TYpos. It also makes sure that **'eric'**, **'Eric'**, and **'ERIC'** are not considered three different people.

- Some of the most common cases are `.lower()`, `.title()`, and `.upper()`.

  ```python
  
  first_name = 'eric'

  print (first_name) # prints the name as-is
  print (first_name.title()) # prints with the first letter capitalized
  print (first_name.upper()) # prints with all letters capitalized

  first_name = 'Eric'
  print (first_name.lower()) # prints with all letters lowercase
  
  ```

- You will see this syntax quite often, where a variable name is followed by a dot and then the name of an action, followed by a set of parentheses. The parentheses may be empty, or they may contain some values.

  ```python
  
  variable_name.action()
  
  ```

- In this example, the word `action` is the name of a **method**. A **method** is something that can be done to a variable.
    - The methods `lower`, `title`, and `upper` are all functions that have been written into the Python language, which do something to strings. Later on, you will learn to write your own methods.

## Combining strings

- It is often very useful to be able to combine strings into a message or page element that we want to display. Again, this is easier to understand through an example.

  ```python

  first_name = 'ada'
  last_name = 'lovelace'

  full_name = first_name + ' ' + last_name

  print (full_name.title()) # outputs: Ada Lovelace

  ```

- The plus sign combines two strings into one, which is called **concatenation**. You can use as many plus signs as you want in composing messages. In fact, many web pages are written as giant strings which are put together through a long series of string concatenations.

  ```python

  first_name = 'ada'
  last_name = 'lovelace'
  full_name = first_name + ' ' + last_name

  message = full_name.title() + ' ' + "was considered the world's first computer programmer."

  print (message) # outputs: Ada Lovelace was considered the world's first computer programmer.

  ```

- If you don't know who Ada Lovelace is, you might want to go read what [Wikipedia](https://en.wikipedia.org/wiki/Ada_Lovelace) or the [Computer History Museum](https://www.computerhistory.org/babbage/adalovelace/) have to say about her. Her life and her work are also the inspiration for the Ada Initiative, which supports women who are involved in technical fields.

## Whitespace

- The term **whitespace** refers to characters that the computer is aware of, but are invisible to readers. The most common whitespace characters are spaces, tabs, and newlines.

- Spaces are easy to create, because you have been using them as long as you have been using computers.

- Tabs and newlines are represented by special character combinations.

- The two-character combination `\t` makes a tab appear in a string. Tabs can be used anywhere you like in a string.

  ```python

  print ("Hello everyone!")
  print ("\tHello everyone!")
  print ("Hello \teveryone!")

  ```

- The combination `\n` makes a newline appear in a string. You can use newlines anywhere you like in a string.

  ```python

  print ("Hello everyone!")
  print ("\nHello everyone!")
  print ("Hello \neveryone!")
  print ("\n\n\nHello everyone!")

  ```

### Stripping whitespace

- Many times you will allow users to enter text into a box, and then you will read that text and use it. It is really easy for people to include extra whitespace at the beginning or end of their text. Whitespace includes spaces, tabs, and newlines.

- It is often a good idea to strip this whitespace from strings before you start working with them. For example, you might want to let people log in, and you probably want to treat 'eric ' as 'eric' when you are trying to see if I exist on your system.

- You can strip whitespace from the left side, the right side, or both sides of a string.

  ```python

  name = ' eric '

  print (name.lstrip())
  print (name.rstrip())
  print (name.strip())

  ```

- It's hard to see exactly what is happening, so maybe the following will make it a little more clear:

  ```python

  name = ' eric '

  print('-' + name.lstrip() + '-')
  print('-' + name.rstrip() + '-')
  print('-' + name.strip() + '-')

  ```

## Strings Further Reading

...

## Strings Problems
1. [Someone Said](#)
   
   Find a quote that you like. Store the quote in a variable, with an appropriate introduction such as "Ken Thompson once said, 'One of my most productive days was throwing away 1000 lines of code'". Print the quote.

1. [First Name Cases](#)

   Store your first name, in lowercase, in a variable. Using that one variable, print your name in lowercase, Titlecase, and UPPERCASE.

1. [Full Name](#)

   Store your first name and last name in separate variables, and then combine them to print out your full name.

1. [About This Person](#)

   Choose a person you look up to. Store their first and last names in separate variables. Use concatenation to make a sentence about this person, and store that sentence in a variable. Print the sentence.

1. [Name Strip](#)

   Store your first name in a variable, but include at least two kinds of whitespace on each side of your name. Print your name as it is stored. Print your name with whitespace stripped from the left side, then from the right side, then from both sides.
