# 🧠 Python and Data Science Notes

---

## 📚 Dictionary Indexing in Python

In Dictionary:
- The first `[]` bracket represents the **column/key**.
- The second `[]` bracket is used to define the **conditional statements**.

---

## 🔢 Features vs Labels in Machine Learning

In Python, especially in machine learning:

- **Features** = Input variables (independent variables) — usually **columns**
- **Labels** = Output variable (target or dependent variable) — usually **rows**

---

## ⚙️ Collective Operators

Collective operators are accessed using the `.` (dot) operator.

---

## 🔍 Finding Index in a List

```python
variable.index(value)

🧩 One is known as One Module
❓ Why Use Jupyter Instead of VS Code?
For implementing the modular approach, Jupyter offers several advantages:

1. ✅ Interactive Development
Run code cell by cell

View outputs immediately, including plots and tables

Great for data exploration, machine learning, and prototyping

2. 🎨 Rich Visualizations
Libraries like Matplotlib, Seaborn, Plotly work seamlessly

Easy to visualize and tweak data in real-time

3. 📝 Inline Documentation
Supports Markdown, LaTeX equations, and rich text

Ideal for teaching, research, and report generation

4. 🧰 Easy Debugging for Beginners
Smaller code chunks (cells)

Easier to isolate and debug

5. 📊 Widely Used in Data Science
Tools like Pandas, NumPy, scikit-learn, and TensorFlow are well integrated

🧱 Architecture of a Data Science Project
Import the library

Data Loading

EDA (Exploratory Data Analysis)

Visualization

Model Training

Prediction

Storytelling

⚠️ Collinearity in Features
If two columns are highly dependent and both are in the input set, we should avoid putting them together.

This property is called Collinearity.

The range of collinearity lies between 0 and 1.

📓 IPyNB
IPyNB stands for Integrated Python Notebook (Jupyter Notebook file format).

⚡ What is Kernel?
A Kernel is responsible for:

Converting binary to electrical signals and vice versa

Managing code execution in notebooks

📄 Markdown File in Python
A Markdown file (.md) is a lightweight file format used for writing formatted text using plain text.

💡 Use Cases:
Write documentation (e.g., README.md)

Create notes, blogs, and reports

Convert to HTML or PDF

Add formatted text in Jupyter Notebooks

🔤 Markdown Syntax (Quick Glance):
# Heading 1
## Heading 2

**Bold Text**
*Italic Text*

- Bullet list
1. Numbered list

`inline code`

```python
# code block in markdown
print("Hello, Markdown!")

Link to Google:

---

## ✅ How to Work with Markdown in Python

### 1. 📝 Create Markdown Files in Python

```python
with open("example.md", "w") as file:
    file.write("# My Markdown\n")
    file.write("This is **bold** and this is *italic*.\n")

🔄 Type Conversion in Python
🔹 Implicit vs Explicit Conversion
Implicit type casting happens automatically — usually from lower to higher data types.

Explicit type casting is done manually using functions like int(), float(), str().

🧠 NumPy and Aliases:
import numpy as np

np is the alias commonly used for the NumPy library in Python.
This allows access to NumPy functions using the np. prefix.

🧾 Import Statements in Python
Collective Import:import library_name

Selective Import:from library_name import module_name

🖨️ Printing Array in NumPy (Slicing):

print(arr2d[:2, :2])


🧬 Data Types in NumPy (Type Conversion)
Symbol	Description
f	float
i	integer
u	unsigned integer
b	boolean
c	complex float
S	string
m	time delta
M	date/time
O	object (generic)
V	void (raw data)


