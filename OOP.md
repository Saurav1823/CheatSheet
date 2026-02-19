## 🧠 Object-Oriented Programming (OOP) in Python

---

## 1️⃣ Introduction to OOP

Object-Oriented Programming (OOP) is a way of structuring programs using **objects** and **classes**.

- A **class** defines structure and behavior.
- An **object** is a real instance created from a class.

OOP makes code:

- Organized
- Reusable
- Easier to scale
- Easier to maintain

---

## 2️⃣ Creating a Class and Object

A class works like a template.  
Objects are created from that template.

```python
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def show_details(self):
        print(f"Name: {self.name}, Age: {self.age}")


student1 = Student("Abhay", 21)
student1.show_details()
```

**Output**
```
Name: Abhay, Age: 21
```

---

## 3️⃣ The Constructor (`__init__`)

The constructor is a special method that runs automatically when an object is created.

It is mainly used to initialize object data.

```python
class Car:
    def __init__(self, brand):
        self.brand = brand


car1 = Car("BMW")
print(car1.brand)
```

**Output**
```
BMW
```

---

## 4️⃣ Instance Variables and Methods

- **Instance variables** store object-specific data.
- **Instance methods** define object behavior.

```python
class Person:
    def __init__(self, name):
        self.name = name

    def greet(self):
        print(f"Hi, I am {self.name}")


p1 = Person("Abhay")
p1.greet()
```

**Output**
```
Hi, I am Abhay
```

---

## 5️⃣ Core Concepts of OOP

OOP is built around four main principles:

- Encapsulation  
- Inheritance  
- Polymorphism  
- Abstraction  

---

## 5.1️⃣ Encapsulation

Encapsulation means combining data and methods inside a class  
and restricting direct access to certain data.

```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance   # private attribute

    def deposit(self, amount):
        self.__balance += amount

    def check_balance(self):
        return self.__balance


account = BankAccount(1000)
account.deposit(500)
print(account.check_balance())
```

**Output**
```
1500
```

Private variables protect internal data.

---

## 5.2️⃣ Inheritance

Inheritance allows one class to reuse features of another class.

```python
class Animal:
    def speak(self):
        print("Animal makes a sound")


class Dog(Animal):
    def bark(self):
        print("Dog barks")


dog = Dog()
dog.speak()
dog.bark()
```

**Output**
```
Animal makes a sound
Dog barks
```

The child class gets access to parent behavior.

---

## 5.3️⃣ Polymorphism

Polymorphism allows different objects to respond to the same method name in different ways.

```python
class Cat:
    def sound(self):
        print("Meow")


class Dog:
    def sound(self):
        print("Bark")


animals = [Cat(), Dog()]

for animal in animals:
    animal.sound()
```

**Output**
```
Meow
Bark
```

Same method name → different behavior.

---

## 5.4️⃣ Abstraction

Abstraction hides complex logic and exposes only necessary functionality.

```python
from abc import ABC, abstractmethod


class Shape(ABC):

    @abstractmethod
    def area(self):
        pass


class Square(Shape):
    def __init__(self, side):
        self.side = side

    def area(self):
        return self.side * self.side


square = Square(4)
print(square.area())
```

**Output**
```
16
```

The abstract class defines structure,  
the child class provides implementation.

---

## 6️⃣ Class Variables vs Instance Variables

- **Class variables** are shared among all objects.
- **Instance variables** are unique for each object.

```python
class Employee:
    company = "TCS"   # shared by all employees

    def __init__(self, name):
        self.name = name


emp1 = Employee("Abhay")
emp2 = Employee("Rahul")

print(emp1.company)
print(emp2.name)
```

**Output**
```
TCS
Rahul
```

---

## 7️⃣ Types of Methods in Python

---

## 7.1️⃣ Instance Method

Works with object data.

```python
class Example:
    def show(self):
        print("This is an instance method")


Example().show()
```

**Output**
```
This is an instance method
```

---

## 7.2️⃣ Class Method

Works with class-level data.

```python
class Example:
    value = 50

    @classmethod
    def display(cls):
        print(cls.value)


Example.display()
```

**Output**
```
50
```

---

## 7.3️⃣ Static Method

Does not depend on class or instance variables.

```python
class Calculator:
    @staticmethod
    def add(a, b):
        return a + b


print(Calculator.add(5, 3))
```

**Output**
```
8
```

---

## 8️⃣ Custom Object Representation (`__str__`)

The `__str__` method defines how an object appears when printed.

```python
class Book:
    def __init__(self, title):
        self.title = title

    def __str__(self):
        return f"Book: {self.title}"


book = Book("Python Basics")
print(book)
```

**Output**
```
Book: Python Basics
```

---

## 9️⃣ Why Use OOP?

- Encourages modular programming  
- Improves code readability  
- Promotes reusability  
- Makes debugging easier  
- Models real-world systems effectively  

---

