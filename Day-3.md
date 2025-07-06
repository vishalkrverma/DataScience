# 🔷 Python Functions

Functions are reusable blocks of code that perform a specific task. They help in organizing code and promoting reusability.

---

## 🔹 Lambda Functions

A **lambda function** is an anonymous (unnamed) function defined using the `lambda` keyword.

### Syntax:
```python
lambda arguments: expression
Example:
g = lambda x: x * x * x
print(g(3))  # Output: 27

🔸 Lambda with filter()
The filter() function is used to filter elements from a list based on a condition.
l1 = [73, 383, 43, 2, 4, 2, 4, 546, 6]
final_list = list(filter(lambda x: (x % 2 != 0), l1))
print(final_list)  # Output: [73, 383, 43]

🔸 Lambda with map()
The map() function is used to apply a function to each element in a list.
li = [1, 2, 3, 4, 5, 67]
list_final = list(map(lambda x: x * 2, li))
print(list_final)  # Output: [2, 4, 6, 8, 10, 134]

🔸 Lambda with reduce()
from functools import reduce
li = [1, 2, 3, 4, 5, 67]
total_sum = reduce(lambda x, y: x + y, li)
print(total_sum)  # Output: 82


🧱 Object-Oriented Programming (OOP) in Python
Object-Oriented Programming (OOP) is a paradigm based on the concept of "objects", which can contain data and methods. Python is a multi-paradigm language and supports OOP fully.

🔹 Key OOP Concepts in Python
1. Class:
class Person:
    def __init__(self, name):
        self.name = name

    def greet(self):
        print("Hello, my name is", self.name)


2. Object:
p1 = Person("Alice")
p1.greet()  # Output: Hello, my name is Alice

3. __init__ Constructor:
class Car:
    def __init__(self, model, year):
        self.model = model
        self.year = year


4. self Keyword
Used to refer to the current object instance within a class.

5. Encapsulation:
   class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # private

    def get_balance(self):
        return self.__balance

6. Inheritance:
class Animal:
    def speak(self):
        print("Animal speaks")
class Dog(Animal):
    def speak(self):
        print("Dog barks")
d = Dog()
d.speak()

7. Polymorphism:
class Bird:
    def fly(self):
        print("Bird can fly")

class Ostrich(Bird):
    def fly(self):
        print("Ostrich can't fly")

b = Bird()
o = Ostrich()
b.fly()
o.fly()

8. Abstraction:
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius

🔸 Summary of OOP Pillars
Concept	Description:
Encapsulation	Hiding internal state and requiring interaction through methods
Inheritance	Deriving new classes from existing ones
Polymorphism	Same interface, different implementation
Abstraction	Hiding complexity, exposing essentials

🧠 Advanced OOP Concepts in Python (Interview-Focused)
While Python supports classical OOP principles, interviews often explore deeper concepts and real-world design scenarios. Here are complex and commonly asked OOP topics with explanations and examples.

1. 🔁 Multiple Inheritance
Python supports multiple inheritance, where a class can inherit from more than one parent class.

class A:
    def method(self):
        print("Method in A")

class B:
    def method(self):
        print("Method in B")

class C(A, B):
    pass
c = C()
c.method()  # Output: Method in A (due to MRO)

2. 🔄 Method Resolution Order (MRO)
Python uses C3 linearization algorithm for MRO. You can inspect the order using ClassName.__mro__ or help(ClassName).

print(C.__mro__)

3. 🧬 Composition vs Inheritance
Inheritance: "is-a" relationship
Composition: "has-a" relationship (more flexible)
class Engine:
    def start(self):
        print("Engine started")

class Car:
    def __init__(self):
        self.engine = Engine()  # Composition

    def drive(self):
        self.engine.start()
        print("Car is moving")

car = Car()
car.drive()

💡 Tip: Prefer composition over inheritance for better code reusability and testability.

4. 🏗️ Class vs Static vs Instance Methods
class MyClass:
    def instance_method(self):
        return "Called instance method"

    @classmethod
    def class_method(cls):
        return "Called class method"

    @staticmethod
    def static_method():
        return "Called static method"

obj = MyClass()
print(obj.instance_method())
print(MyClass.class_method())
print(MyClass.static_method())


Method Type	Accesses	Use Case
Instance Method	      self	Instance-specific logic.
Class Method	        cls	Factory methods, alter class state.
Static Method	None   	Utility/helper logic.

5. 🧱 Dunder (Magic) Methods
These are special methods with double underscores that enable operator overloading and object customization.

Common Dunder Methods:
Method	     Purpose
__init__	   Constructor
__str__	     String representation
__len__	     Length using len()
__add__      Overload + operator
__eq__	     Equality comparison

Example:
class Book:
    def __init__(self, pages):
        self.pages = pages

    def __add__(self, other):
        return self.pages + other.pages

book1 = Book(100)
book2 = Book(200)
print(book1 + book2)  # Output: 300

6. 🎭 Duck Typing
"If it walks like a duck and quacks like a duck..."
Python focuses on behavior, not type.

class Duck:
    def quack(self):
        print("Quack!")
class Person:
    def quack(self):
        print("I'm quacking like a duck!")
def make_it_quack(entity):
    entity.quack()
make_it_quack(Duck())    # Quack!
make_it_quack(Person())  # I'm quacking like a duck!

✅ Key Insight: Python uses dynamic typing, enabling flexibility in polymorphism.

7. 🚦Access Modifiers in Python
Python doesn't enforce access modifiers but uses conventions:

Modifier	Syntax	Meaning
Public	var	Accessible everywhere
Protected	_var	Internal use (suggested)
Private	__var	Name mangling for access control

class Demo:
    def __init__(self):
        self.public = "Public"
        self._protected = "Protected"
        self.__private = "Private"

obj = Demo()
print(obj.public)
print(obj._protected)
# print(obj.__private)  # Error
print(obj._Demo__private)  # Access via name mangling


8. 🧩 SOLID Principles (Optional but High-Value)
Principle	Description
S: Single Responsibility	A class should have one job
O: Open/Closed	Open for extension, closed for modification
L: Liskov Substitution	Derived classes should substitute base classes
I: Interface Segregation	No client should depend on unused methods
D: Dependency Inversion	Depend on abstractions, not concretions

9. 🧠 Real Interview Questions
What is the difference between composition and inheritance?

Explain Python’s MRO and how it handles method conflict.

What are @classmethod and @staticmethod used for?

How is abstraction implemented in Python?

Can you explain duck typing with an example?

How does Python support multiple inheritance safely?

How can you prevent a class from being inherited?


