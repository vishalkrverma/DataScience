# 🧠 NumPy: Copy vs View, Reshaping, Joining, Stacking, Searching, Filtering

## 🔹 Jupyter Markdown Note

To create a Markdown cell in Jupyter, press:

```plaintext
Esc + M
🔸 Copy vs View in NumPy
View is used to create a new array referencing the same memory.
If changes are made in the new array, the original array is also affected.

Copy creates a separate array with its own memory.
Changes in the new array do not affect the original.

🧠 Difference Between .copy() and .view()
Feature	.copy()	.view()
Type	Deep copy	Shallow copy
Memory Sharing	Independent memory	Shares memory with original array
Changes Reflect?	No	Yes
Use Case	When you need a separate clone	When you need a different view without duplicating data

📌 Summary

Use .copy() to preserve original data.

Use .view() for memory-efficient reshaped/sliced views.

🔹 NumPy Array Attributes
Use .ndim to check number of dimensions.
import numpy as np
arr = np.array([1, 2, 3, 4], ndmin=5)
print(arr)
print('Number of dimensions:', arr.ndim)

🔹 Accessing 2-D Arrays
Think of 2D arrays like tables:
arr = np.array([[1, 2, 3], [4, 5, 6]])
print(arr[0, 2])  # Access element at first row, third column

🔹 Data Types and Type Conversion
✅ Check Data Type
arr = np.array([1, 2, 3, 4], dtype='S')
print(arr.dtype)

✅ Set 4-byte integer type
arr = np.array([1, 2, 3, 4], dtype='i4')
print(arr.dtype)

✅ Convert Float to Integer
arr = np.array([1.1, 2.1, 3.1])
newarr = arr.astype('i')
print(newarr)
print(newarr.dtype)
newarr = arr.astype(int)

🔹 Reshaping Arrays
Reshape 1D → 3D
arr = np.array([1,2,3,4,5,6,7,8,9,10,11,12])
newarr = arr.reshape(2, 3, 2)
print(newarr)
Using Unknown Dimension (-1)
unknown2d = arr.reshape(2, -1)
print(unknown2d)
print(unknown2d.shape)
⚠️ You can only use one -1 in the reshape.

🔹 Joining Arrays
Concatenate 2D Arrays by Columns:
arr1 = np.array([[1, 2], [3, 4]])
arr2 = np.array([[5, 6], [7, 8]])
arr = np.concatenate((arr1, arr2), axis=1)
print(arr)
🔹 Stacking Arrays:
Stack Along New Axis

arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])
arr = np.stack((arr1, arr2), axis=1)
print(arr)

Horizontal Stack (hstack)
arr = np.hstack((arr1, arr2))

Vertical Stack (vstack)
arr = np.vstack((arr1, arr2))
Depth Stack (dstack)
arr = np.dstack((arr1, arr2))

🔹 Splitting Arrays
arr = np.array([1,2,3,4,5,6,7,8])
newarr = arr.reshape(2, 2, -1)
print(newarr)
📌 Note: Result is a list of arrays. Use indexing or loop to access.

🔹 Flattening Arrays
Convert N-D array to 1D:
flat = arr.reshape(-1)
Also explore: .flatten(), .ravel(), flip(), rot90() for advanced reshaping.

🔹 Searching in Arrays
Find Index Where Value = 4
arr = np.array([1, 2, 3, 4, 5, 4, 4])
x = np.where(arr == 4)
print(x)

Search Sorted (Binary Search)
arr = np.array([6, 7, 8, 9])
x = np.searchsorted(arr, 7, side='right')
print(x)

🔹 Filtering Arrays
Manual Filtering
arr = np.array([41, 42, 43, 44])
x = [True, False, True, False]
newarr = arr[x]
print(newarr)  # [41, 43]

Create Filter Based on Condition:
filter_arr = arr > 42
newarr = arr[filter_arr]
print(newarr)

Or use a loop:
filter_arr = []
for element in arr:
    filter_arr.append(element > 42)
newarr = arr[filter_arr]
