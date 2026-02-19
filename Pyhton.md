##  Python Cheat Sheet

---

## 1️⃣ Variables

```python
a = 10
name = "Saurav"

print(a)
print(name)
```

**Output**
```
10
Saurav
```

---

## 2️⃣ Data Types

```python
print(type(10))
print(type(3.14))
print(type("Hello"))
print(type(True))
print(type([1,2]))
print(type((1,2)))
print(type({"a":1}))
print(type({1,2}))
```

**Output**
```
<class 'int'>
<class 'float'>
<class 'str'>
<class 'bool'>
<class 'list'>
<class 'tuple'>
<class 'dict'>
<class 'set'>
```

---

## 3️⃣ Type Conversion

```python
print(int("10"))
print(float("3.14"))
print(str(100))
print(bin(10))
print(hex(10))
print(oct(10))
print(chr(65))
print(ord("A"))
```

**Output**
```
10
3.14
100
0b1010
0xa
0o12
A
65
```

---

## 4️⃣ Operators

```python
print(5 + 2)
print(5 - 2)
print(5 * 2)
print(5 / 2)
print(5 % 2)
print(5 ** 2)
print(5 // 2)
```

**Output**
```
7
3
10
2.5
1
25
2
```

---

## 5️⃣ Conditional Statements

```python
age = 20

if age >= 18:
    print("Adult")
elif age > 12:
    print("Teen")
else:
    print("Child")
```

**Output**
```
Adult
```

---

## 6️⃣ Loops

### For Loop

```python
for i in range(3):
    print(i)
```

**Output**
```
0
1
2
```

### While Loop

```python
x = 1
while x <= 3:
    print(x)
    x += 1
```

**Output**
```
1
2
3
```

---

## 7️⃣ Functions

```python
def greet(name):
    return f"Hello {name}"

print(greet("Saurav"))
```

**Output**
```
Hello Saurav
```

---

## 8️⃣ Lambda Function

```python
add = lambda a, b: a + b
print(add(3, 4))
```

**Output**
```
7
```

---

## 9️⃣ List

```python
nums = [1, 2, 3]

nums.append(4)
nums.extend([5, 6])
nums.insert(0, 0)
nums.remove(3)
nums.pop()
nums.sort()
nums.reverse()

print(nums)
print(len(nums))
```

**Output**
```
[5, 4, 2, 1, 0]
5
```

---

## 🔟 Tuple

```python
t = (1, 2, 3)
print(t[0])
print(len(t))
```

**Output**
```
1
3
```

---

## 1️⃣1️⃣ Set

```python
s = {1, 2, 3}
s.add(4)
s.remove(2)
print(s)
```

**Output**
```
{1, 3, 4}
```

---

## 1️⃣2️⃣ Dictionary

```python
d = {"a": 1}

print(d.get("a"))
print(d.keys())
print(d.values())
print(d.items())

d.update({"b": 2})
d.pop("a")

print(d)
```

**Output**
```
1
dict_keys(['a'])
dict_values([1])
dict_items([('a', 1)])
{'b': 2}
```

---

## 1️⃣3️⃣ String Methods

```python
print("HELLO".lower())
print("hello".upper())
print("  hi  ".strip())
print("apple".replace("a", "A"))
print("a,b,c".split(","))
print(",".join(["a", "b", "c"]))
print("banana".count("a"))
print("hello".find("e"))
```

**Output**
```
hello
HELLO
hi
Apple
['a', 'b', 'c']
a,b,c
3
1
```

---

## 1️⃣4️⃣ Built-in Functions

```python
print(abs(-10))
print(round(3.456, 2))
print(pow(2, 4))
print(divmod(10, 3))
print(sum([1, 2, 3]))
print(max([1, 5, 2]))
print(min([1, 5, 2]))
print(list(range(5)))
print(sorted([3, 1, 2]))
print(list(reversed([1, 2, 3])))
```

**Output**
```
10
3.46
16
(3, 1)
6
5
1
[0, 1, 2, 3, 4]
[1, 2, 3]
[3, 2, 1]
```

---

## 1️⃣5️⃣ Functional Built-ins

```python
nums = [1, 2, 3, 4]

print(list(map(lambda x: x * 2, nums)))
print(list(filter(lambda x: x % 2 == 0, nums)))
print(list(zip([1, 2], ["a", "b"])))
print(any([False, True, False]))
print(all([True, True, False]))
```

**Output**
```
[2, 4, 6, 8]
[2, 4]
[(1, 'a'), (2, 'b')]
True
False
```

---

## 1️⃣6️⃣ enumerate()

```python
names = ["A", "B", "C"]

for index, value in enumerate(names):
    print(index, value)
```

**Output**
```
0 A
1 B
2 C
```

---

## 1️⃣7️⃣ List Comprehension

```python
squares = [x * x for x in range(5)]
print(squares)
```

**Output**
```
[0, 1, 4, 9, 16]
```

---

## 1️⃣8️⃣ Exception Handling

```python
try:
    print(10 / 0)
except ZeroDivisionError:
    print("Cannot divide by zero")
```

**Output**
```
Cannot divide by zero
```

---

## 1️⃣9️⃣ File Handling

```python
with open("sample.txt", "w") as f:
    f.write("Hello World")

with open("sample.txt", "r") as f:
    print(f.read())
```

**Output**
```
Hello World
```

---

## 2️⃣0️⃣ Classes & Objects

```python
class Student:
    def __init__(self, name):
        self.name = name

    def show(self):
        print("Student:", self.name)

s = Student("Rahul")
s.show()
```

**Output**
```
Student: Rahul
```

---


