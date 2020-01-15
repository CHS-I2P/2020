# Strings

## Notes

Strings are sets of characters. Strings are easier to understand by looking at some examples.

### Single and double quotes

- Strings are contained by either single or double quotes.

  ```python
  my_string = "This is a double-quoted string."
  my_string = 'This is a single-quoted string.'
  ```

- This lets us make strings that contain quotations.

  ```python
  quote = "Linus Torvalds once said, 'Any program is only as good as it is useful.'"
  ```

### Changing case

- You can easily change the case of a string, to present it the way you want it to look.

- It is often good to store data in lower case, and then change the case as you want to for presentation. This catches some TYpos. It also makes sure that **'eric'**, **'Eric'**, and **'ERIC'** are not considered three different people.

- Some of the most common cases are `.lower()`, `.title()`, and `.upper()`.

  ```python
  
  first_name = 'eric'

  print (first_name) # prints the name as-is
  print (first_name.title()) # prints with the first letter capitalized
  print (first_name.upper()) # prints with all letters capitalized

  first_name = 'Eric'
  print(first_name.lower()) # prints with all letters lowercase
  
  ```

- You will see this syntax quite often, where a variable name is followed by a dot and then the name of an action, followed by a set of parentheses. The parentheses may be empty, or they may contain some values.

variable_name.action()

In this example, the word "action" is the name of a method. A method is something that can be done to a variable. The methods 'lower', 'title', and 'upper' are all functions that have been written into the Python language, which do something to strings. Later on, you will learn to write your own methods.

Combining strings (concatenation)
It is often very useful to be able to combine strings into a message or page element that we want to display. Again, this is easier to understand through an example.

first_name = 'ada'
last_name = 'lovelace'

full_name = first_name + ' ' + last_name

print(full_name.title())
The plus sign combines two strings into one, which is called "concatenation". You can use as many plus signs as you want in composing messages. In fact, many web pages are written as giant strings which are put together through a long series of string concatenations.

first_name = 'ada'
last_name = 'lovelace'
full_name = first_name + ' ' + last_name

message = full_name.title() + ' ' + "was considered the world's first computer programmer."

print(message)
If you don't know who Ada Lovelace is, you might want to go read what Wikipedia or the Computer History Museum have to say about her. Her life and her work are also the inspiration for the Ada Initiative, which supports women who are involved in technical fields.

Whitespace
The term "whitespace" refers to characters that the computer is aware of, but are invisible to readers. The most common whitespace characters are spaces, tabs, and newlines.

Spaces are easy to create, because you have been using them as long as you have been using computers. Tabs and newlines are represented by special character combinations.

The two-character combination "\t" makes a tab appear in a string. Tabs can be used anywhere you like in a string.

print("Hello everyone!")
print("\tHello everyone!")
print("Hello \teveryone!")
The combination "\n" makes a newline appear in a string. You can use newlines anywhere you like in a string.

print("Hello everyone!")
print("\nHello everyone!")
print("Hello \neveryone!")
print("\n\n\nHello everyone!")
Stripping whitespace
Many times you will allow users to enter text into a box, and then you will read that text and use it. It is really easy for people to include extra whitespace at the beginning or end of their text. Whitespace includes spaces, tabs, and newlines.

It is often a good idea to strip this whitespace from strings before you start working with them. For example, you might want to let people log in, and you probably want to treat 'eric ' as 'eric' when you are trying to see if I exist on your system.

You can strip whitespace from the left side, the right side, or both sides of a string.

name = ' eric '

print(name.lstrip())
print(name.rstrip())
print(name.strip())
It's hard to see exactly what is happening, so maybe the following will make it a little more clear:

name = ' eric '

print('-' + name.lstrip() + '-')
print('-' + name.rstrip() + '-')
print('-' + name.strip() + '-')

Exercises
Someone Said
Find a quote that you like. Store the quote in a variable, with an appropriate introduction such as "Ken Thompson once said, 'One of my most productive days was throwing away 1000 lines of code'". Print the quote.
First Name Cases
Store your first name, in lowercase, in a variable.
Using that one variable, print your name in lowercase, Titlecase, and UPPERCASE.
Full Name
Store your first name and last name in separate variables, and then combine them to print out your full name.
About This Person
Choose a person you look up to. Store their first and last names in separate variables.
Use concatenation to make a sentence about this person, and store that sentence in a variable.-
Print the sentence.
Name Strip
Store your first name in a variable, but include at least two kinds of whitespace on each side of your name.
Print your name as it is stored.
Print your name with whitespace stripped from the left side, then from the right side, then from both sides.
