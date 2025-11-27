# python-practical

# Functions and Modules:
# functions
A function is a block of reusable code that performs a specific task.It helps avoid code repetition and makes programs modular.
def add(a, b):
    return a + b

def function_name(parameters):

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
2 nd way
def greet(name):

    print("Hello", name)

greet("Alice")


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

Write a function to generate Fibonacci sequence.


def fibonacci(n):
    a, b = 0, 1
    for i in range(n):
        print(a, end=" ")
        a, b = b, a + b

# What is a decorator?
A decorator is a function that modifies the behavior of another function without changing its actual code.
# Why Are Decorators Used?
Logging ,Authentication,Performance measurement,Access control,Input validation


# What is a generator?
A generator is a function that yields values one by one using yield instead of return.

# yield pauses and resumes the function saving memory;
# return ends the function immediately.

# Write a generator to produce numbers from 1 to 5.

def gen_nums():
    for i in range(1, 6):
        yield i

for n in gen_nums():
    print(n)
2nd way
    for i in range(1, 6):
    print(i)
    
# What is an Iterator?
An iterator is an object in Python that allows you to loop through a sequence (like list, tuple, string) one item at a time.

An iterator must implement two methods:

 __iter__() → returns the iterator object
 __next__() → returns the next value; raises StopIteration when finished

#  What is a lambda function?
 A lambda function is an anonymous, one-line function created using the lambda keyword.

# Use lambda with map() to add 10 to each number in a list.(square numbers, uppercase)
map() is used when we want to transform each element in a list."

nums = [1, 2, 3]

result = list(map(lambda x: x + 10, nums))

print(result)  

# Use lambda with filter() to get only even numbers. even numbers
filter() keeps ONLY those items for which the function returns True. "filter() is used to filter items from a list based on a condition.

nums = [1, 2, 3, 4, 5, 6]

evens = list(filter(lambda x: x % 2 == 0, nums))

print(evens)

# Filter names starting with 'A'

names = ["Arun", "Bob", "Akhil", "John"]

result = list(filter(lambda x: x.startswith('A'), names))

print(result)

# reduce()
reduces a list into a single value. reduce() applies a function cumulatively and collapses the list into one result (like sum, product, max)."
Sum of all numbers
from functools import reduce

nums = [1, 2, 3, 4]

total = reduce(lambda a, b: a + b, nums)

print(total)

# What is a User-Defined Function?
“A UDF is a function created by the programmer using the def keyword. It helps avoid repeated code, improves readability, and makes programs modular.”

def function_name(parameters):
    return value





