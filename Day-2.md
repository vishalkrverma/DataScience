# Python Basics Notes

## ✅ Python Keywords

Keywords are reserved words in Python. They are case-sensitive and cannot be used as identifiers.

```python
import keyword

print(keyword.kwlist)
print("\nTotal number of keywords:", len(keyword.kwlist))

🔠 Identifiers
Identifiers are the names given to entities like classes, functions, variables, etc.

Rules:
Must start with a letter (A-Z, a-z) or underscore (_)

Cannot start with a digit.
Cannot use keywords.
Case-sensitive.

# Valid identifiers
my_var = 10
_age = 25
Name1 = "John"

# Invalid identifiers
# 1name = "Invalid"
# class = "Keyword used"

💬 Comments in Python
Single line: Starts with #

Multi-line: Enclosed with triple quotes ''' or """

# This is a single line comment

"""
This is a
multi-line comment
"""

🔄 Multiline Statements
By default, Python considers a line break as the end of a statement. To continue a line:

Using backslash \:
a = 1 + 2 + 3 + \
    4 + 5 + 6 + \
    7 + 8
print(a)

Using brackets (), [], {}:
numbers = (1 + 2 + 3 +
           4 + 5 + 6)
print(numbers)

📦 Variables and Assignments
A variable is a storage location for data.

Multiple Assignments:
a, b, c = 10, 5.5, "AAAL"
print(a, b, c)

Assigning same value to multiple variables:
a = b = c = "qrj"
print(a, b, c)

🧠 Memory Address of Variable
To print the memory address (ID):
x = 100
print(id(x))

Everything in Python is an object.

🔤 Strings in Python
A string is a sequence of Unicode characters.

Strings can be enclosed in ', ", or triple quotes ''' or """.

s = "Hello"
print(s[0])  # H

multi_line = """This
is a multiline
string"""
print(multi_line)


📋 List and Tuple
✅ List
Mutable
Ordered
Can contain different data types:
my_list = [1, 2, 3, "Hello"]
my_list[0] = 10
print(my_list)

✅ Tuple
Immutable
Ordered

my_tuple = (1, 2, 3, "Hello")
# my_tuple[0] = 10  # ❌ will give error
print(my_tuple)

⌨️ Input and Output
name = input("Enter your name: ")
print("Hello", name)

Output
a, b = 5, 10
print("Sum is:", a + b)

🔁 Type Conversion:
a = "100"
b = int(a)
print(b + 1)  # Output: 101

Function	Description
int()	Converts to integer
float()	Converts to float
str()	Converts to string
list()	Converts to list

➕ All Types of Operators
1. Arithmetic Operators:
a, b = 10, 3
print(a + b, a - b, a * b, a / b, a % b, a ** b, a // b)

2. Relational (Comparison) Operators:
print(a > b, a < b, a == b, a != b)

3. Logical Operators:
print(True and False, True or False, not True)

4. Bitwise Operators:
print(a & b, a | b, a ^ b, ~a, a << 2, a >> 2)

5. Assignment Operators:
x = 5
x += 3  # same as x = x + 3

6. Identity Operators:

x = [1, 2]
y = [1, 2]
print(x is y, x is not y)  # 'is' checks memory location

7. Membership Operators:
print(1 in [1, 2, 3], 4 not in [1, 2, 3])


❓ Conditional Statements
Used to control the flow based on conditions.

if
x = 10
if x > 5:
    print("Greater than 5")

if-else

x = 3
if x > 5:
    print("Greater")
else:
    print("Smaller or equal")

if-elif-else:
x = 0
if x > 0:
    print("Positive")
elif x == 0:
    print("Zero")
else:
    print("Negative")

Loops in Pyhton:
# 🔁 Loops in Python

Python provides two types of loops:
- `while` loop
- `for` loop

Loops are used to execute a block of code repeatedly.

---

## 🔂 while Loop

The `while` loop keeps executing the block of code **as long as the condition is True**.

### ✅ Syntax:
```python
while condition:
    # code block

📌 Example 1: Print numbers from 1 to 5
i = 1
while i <= 5:
    print(i)
    i += 1

📌 Example 2: Infinite loop with break
i = 1
while True:
    print(i)
    if i == 3:
        break  # exits loop when i is 3
    i += 1

🔁 for Loop
The for loop is used to iterate over a sequence (like list, tuple, string, range).

for variable in sequence:
    # code block

📌 Example 1: Print each element in a list
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)

📌 Example 2: Using range():
for i in range(1, 6):
    print(i)  # prints 1 to 5

🔚 break Statement
break is used to terminate the loop prematurely.

📌 Example: Stop loop when number is 3

for i in range(1, 6):
    if i == 3:
        break
    print(i)
# Output: 1, 2

🔁 continue Statement
continue skips the rest of the code inside the loop for the current iteration and jumps to the next.

📌 Example: Skip number 3
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
# Output: 1, 2, 4, 5


✅ Using while with continue and break
📌 Example: Skip even numbers and stop at 7
i = 0
while i < 10:
    i += 1
    if i % 2 == 0:
        continue  # skip even numbers
    if i == 7:
        break  # stop at 7
    print(i)
# Output: 1, 3, 5
Summary Table
Loop Type	Use Case
while	When condition is checked dynamically
for	When iterating over a sequence
break	To exit loop prematurely
continue	To skip current iteration
