# Variables

## Notes

A variable holds a value.

**input**

```python
message = "Hello Python world!"
print (message)
```

**output**

```
$ Hello Python world!
```

*Note: You can change the value of a variable at any point.*

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

### Naming Rules

1. Variables can only contain letters, numbers, and underscores. Variable names can start with a letter or an underscore, but can not start with a number.
2. Spaces are not allowed in variable names, so we use underscores instead of spaces. For example, use `student_name` instead of `student name`.
3. You cannot use [Python keywords](https://docs.python.org/2.5/ref/keywords.html) as variable names.
4. Variable names should be descriptive, without being too long. For example `mc_wheels` is better than just `wheels`, and `number_of_wheels_on_a_motorycle`.
5. Be careful about using the lowercase letter l and the uppercase letter O in places where they could be confused with the numbers 1 and 0.

### NameError

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

## Further Reading

...

## Problems

1. [My Own Variable](#)

   Using what you've just learned, you'll create your own variable with custom message.
   
1. [One Variable, Two Messages](#)

   In this short problem you'll write one variable that stores two different messages.
