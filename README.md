# NumPy Project

## Project Overview

This project involves various tasks using the NumPy library to create, manipulate, and analyze arrays. The tasks include generating sequences, reshaping arrays, changing data types, and performing operations such as joining and splitting arrays.

## Getting Started

### Prerequisites

Make sure you have Python and NumPy installed. If not, you can install NumPy using pip:
```sh
pip install numpy
```

### Importing the Library

Begin by importing the NumPy library:
```python
import numpy as np
```

## Tasks and Code

### Generating a Sequence of Floats
Generate a sequence of 15 floats using the `linspace()` function:
```python
sequence = np.linspace(0, 1, 15)
print(sequence)
```

### Creating a 3-D Array
Create a 3-D array with the shape (2, 2, 3) containing the specified values:
```python
array_3d = np.array([
    [[1.1, 2.1, 3.1], [4.1, 5.1, 6.1]],
    [[7.1, 8.1, 9.1], [10.1, 11.1, 12.1]]
])
print(array_3d)
```

### Array Details
Print the array's type, elements' data type, shape, size, and dimension:
```python
print("Array's type:", type(array_3d))
print("Array's elements datatype:", array_3d.dtype)
print("Array's shape:", array_3d.shape)
print("Array's size:", array_3d.size)
print("Array's dimension:", array_3d.ndim)
```

### Changing Array Dimension
Change the array's dimension from 3-D to 4-D:
```python
array_4d = array_3d.reshape(2, 2, 1, 3)
print("New array's dimension:", array_4d.ndim)
print("New array's shape:", array_4d.shape)
print(array_4d)
```

### Changing Data Type
Change the array's elements' data type to integer:
```python
array_int = array_4d.astype(int)
print(array_int)
```

### Iterating Over Array Elements
Print all array elements using a for loop:
```python
for elem in np.nditer(array_int):
    print(elem)
```

### Accessing Specific Elements
Print the number 8 using array slicing:
```python
print(array_int[1, 0, 0, 1])
```

Print numbers 5 and 6 using array slicing:
```python
print(array_int[0, 1, 0, 1:])
```

### Searching for an Element
Search for the number 8 using the `where()` function:
```python
indices = np.where(array_int == 8)
print(indices)
```

### Reshaping the Array
Reshape the array to the specified shape:
```python
reshaped_array = array_int.reshape(2, 3, 2)
print(reshaped_array)
```

### Joining Arrays
Join the given arrays without specifying the axis:
```python
arr1 = np.array([['A', 'B'], ['E', 'F']])
arr2 = np.array([['C', 'D'], ['G', 'H']])
joined_array = np.concatenate((arr1, arr2))
print(joined_array)
```

Join the arrays along rows with axis = 1:
```python
joined_array_axis1 = np.concatenate((arr1, arr2), axis=1)
print(joined_array_axis1)
```

### Splitting Arrays
Split the array into two arrays with axis = 1:
```python
split_arrays = np.split(joined_array, 2, axis=1)
print(split_arrays[0])
print(split_arrays[1])
```

## Conclusion

This project demonstrates various NumPy functionalities including array creation, reshaping, type conversion, element access, and array operations. By following the code provided, you can gain a solid understanding of how to use NumPy for array manipulation and analysis.
