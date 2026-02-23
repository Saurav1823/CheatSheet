# Decorators in Python

## Introduction

Decorators in Python are a powerful feature that allows us to modify or extend the behavior of a function without changing its actual code.

They are commonly used for logging, authentication, performance measurement, and access control.

A decorator is a function that takes another function as an argument and returns a new function with added functionality.

---

## Why Use Decorators?

Decorators help in:

- Code reusability
- Clean and readable code
- Separation of concerns
- Adding functionality dynamically

Instead of modifying existing functions, we wrap them with additional behavior.

---

## Basic Concept of Functions as Objects

In Python, functions are first-class objects. This means:

- Functions can be assigned to variables
- Functions can be passed as arguments
- Functions can return other functions

This concept makes decorators possible.

---

## Basic Structure of a Decorator

A decorator consists of:

- A wrapper function
- The original function as an argument
- Returning the wrapper function

### Example

```python
def my_decorator(func):
    def wrapper():
        print("Something before the function runs")
        func()
        print("Something after the function runs")
    return wrapper

@my_decorator
def say_hello():
    print("Hello!")

say_hello()
```

### Output

```
Something before the function runs
Hello!
Something after the function runs
```

---

## How Decorator Works

When we use:

```python
@my_decorator
```

It is equivalent to writing:

```python
say_hello = my_decorator(say_hello)
```

The original function is passed into the decorator, and the returned wrapper function replaces it.

---

## Decorators with Arguments

Decorators can also handle functions that accept parameters.

### Example

```python
def my_decorator(func):
    def wrapper(*args, **kwargs):
        print("Before execution")
        result = func(*args, **kwargs)
        print("After execution")
        return result
    return wrapper

@my_decorator
def add(a, b):
    return a + b

print(add(3, 5))
```

---

## Common Uses of Decorators

- Logging function calls
- Measuring execution time
- Authentication checks
- Access control
- Caching results

---

## Built-in Python Decorators

Python provides several built-in decorators:

- @staticmethod
- @classmethod
- @property

These are commonly used in object-oriented programming.

---

## Advantages of Decorators

- Improves code readability
- Avoids code repetition
- Encourages modular design
- Easy to maintain

---

## Conclusion

Decorators are a powerful and flexible feature in Python that allow programmers to extend the behavior of functions and methods. They promote clean, reusable, and maintainable code by separating additional functionality from the main logic.
