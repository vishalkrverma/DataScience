# Notes on Python, Java, and Computer Fundamentals

---

## 📌 Object-Oriented Concepts: Python vs Java

- **Python** is *purely object-oriented*.
- **Java** depends on usage:
  - Using **Wrapper classes** → purely object-oriented.
  - Using **primitive data types** → not purely object-oriented.
- In Python, **all data are objects** by default.

---

## 📊 Why Data Science with Python?

- Python includes powerful libraries:
  - `NumPy`
  - `Pandas`
  - `Matplotlib`
- These make data analysis and visualization **easy and efficient**.

---

## 🌐 Why is Python Platform Independent?

- Python runs on any OS with a Python interpreter.
- The **interpreter handles platform-specific differences**.
- **Write once, run anywhere** — no recompilation needed.

---

## ⚙️ How Software Executes in an Operating System

1. **Source code** is compiled/interpreted to machine code or bytecode.
2. Executable is loaded into memory by the OS.
3. The OS manages execution via:
   - CPU scheduling
   - Memory management
   - I/O operations
4. Programs use **system calls** to interact with hardware.

---

## 💡 Why Do Computers Use Only 0s and 1s?

- Digital circuits have two stable states: ON and OFF.
- Binary (0 and 1) is **easy to represent and detect** physically.
- Leads to **simpler and more reliable hardware design**.

---

## 🧠 Python vs Other Languages: OS Kernel Interaction

- **Python communicates directly with the kernel**.
- Other languages use system software as an intermediary.
- This can make Python **faster for data-handling operations**.

---

## 🖨️ Print Behavior in Python

- After `print()`, the cursor moves to the **next line**.
- Printing multiple values with commas inserts **spaces automatically**:

```python
print("Hello", "World")
# Output:
# Hello World
