# python-practical

# Functions and Modules:
# functions
A function is a block of reusable code that performs a specific task.It helps avoid code repetition and makes programs modular.
def add(a, b):
    return a + b

def function_name(parameters):      (syntax)
    return value
    
# modules
A module is a Python file (.py) containing variables, functions, or classes.It can be imported and reused in other programs.
mymodule.py

def add(a, b):
    return a + b

# What is *args in Python?
*args allows a function to accept any number of positional arguments.We use it when we don’t know how many values the user will pass.

def add_numbers(*args):                    
    return sum(args)
print(add_numbers(10, 20, 30))  out put 60

def greet(name):
    return f"Hello, {name}!"
print(greet("Alice")) out put hello,alice!

# What is **kwargs in Python?
**kwargs allows a function to accept any number of keyword arguments.We use it when we want to pass data in key-value pairs.

def details(**kwargs):
    print(kwargs)

    result = add(10, 20)
print(result)

# parameter
variable in function definition
# argument
value passed during function call
# What is Recursion?
Recursion is a technique where a function calls itself until a base condition is reached.(mirror inside a mirror)

# package
A package is a collection of modules stored in a directory containg _int_.pyfile

# Basic lambda to check even or odd

check = lambda x: "Even" if x % 2 == 0 else "Odd"

print(check(10))  
print(check(7)) 


# Write a lambda function to add two numbers and print the result.

a = lambda a,b : a+b
print(a(10,20))

# Find the largest of three numbers using lambda

largest = lambda a, b, c: max(a, b, c)
print(largest(10, 25, 15))  # Output: 25

# find the square of a number using lambda

square =  lambda x:x**2
print(square(9))

# Reverse a string without using slicing.

text = "hello"
rev = ""
for ch in text:
    rev = ch + rev     
print(rev)
We take an empty string rev.
✔ We loop through each character in the original string.
✔ Instead of adding characters at the end,
we add each character at the beginning of the new string.

# Check if a string is a palindrome.

text = "madam"
rev = text[::-1]
if text == rev:
    print("Palindrome")
else:
    print("Not a palindrome")
A palindrome is a string that reads the same forwards and backwards.
Example → madam, level, radar
We compare the original string (text) with its reversed version (text[::-1]).
If both are equal → it is a palindrome.

text = "level"    (Using a loop to build the reverse string)
rev = ""
for ch in text:
    rev = ch + rev
if text == rev:
    print("Palindrome")
else:
    print("Not a palindrome")


# Count occurrences of each word in a sentence.

from collections import Counter

sentence = "apple banana apple orange banana apple"
count = Counter(sentence.split())

print(count)

Counter({'apple': 3, 'banana': 2, 'orange': 1})

Counter automatically counts repeated elements.
I pass a list of words into Counter.
It returns a dictionary-like object with word counts.

