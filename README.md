# python-practical

# Functions and Modules:
# functions
A function is a block of reusable code that performs a specific task.It helps avoid code repetition and makes programs modular.
# modules
A module is a Python file (.py) containing variables, functions, or classes.It can be imported and reused in other programs.

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
