# 📝 NumPy Notes

## 1. Creating NumPy Arrays

```python
import numpy as np
```

### Create Arrays

```python
np.array([1, 2, 3])
np.array([[1, 2], [3, 4]])
```

### Generate Arrays

| Function                             | Description                                        |
| ------------------------------------ | -------------------------------------------------- |
| `np.arange(start, stop, step)`       | Creates an array with a given range                |
| `np.random.rand(n)`                  | Random numbers between 0 and 1                     |
| `np.random.randn(n)`                 | Random numbers from a standard normal distribution |
| `np.random.randint(low, high, size)` | Random integers                                    |

Example:

```python
np.arange(1, 20, 3)
np.random.randint(2, 6, 3)
```

---

# 2. Array Attributes

| Attribute  | Description                 |
| ---------- | --------------------------- |
| `shape`    | Dimensions of the array     |
| `size`     | Total number of elements    |
| `ndim`     | Number of dimensions        |
| `dtype`    | Data type of elements       |
| `itemsize` | Size of one element (bytes) |
| `nbytes`   | Total memory used           |

Example:

```python
arr.shape
arr.size
arr.ndim
arr.dtype
arr.itemsize
arr.nbytes
```

---

# 3. Array Methods

| Method     | Purpose                |
| ---------- | ---------------------- |
| `min()`    | Smallest element       |
| `max()`    | Largest element        |
| `sum()`    | Sum of all elements    |
| `mean()`   | Average                |
| `std()`    | Standard deviation     |
| `argmax()` | Index of maximum value |
| `argmin()` | Index of minimum value |

### Sum Along Axis

```python
np.sum(arr, axis=0)   # Column-wise
np.sum(arr, axis=1)   # Row-wise
```

---

# 4. Reshaping Arrays

Change the dimensions without changing the data.

```python
arr = np.arange(1, 31)
arr.reshape(6, 5)
```

---

# 5. Array Indexing

Works exactly like Python lists.

```python
arr[0]
arr[2]
arr[-1]
```

---

# 6. Array Slicing

```python
arr[2:10]
arr[:]
arr[::2]
arr[2:20:3]
```

---

# 7. Matrix Indexing

Syntax:

```python
array[row_start:row_end, column_start:column_end]
```

Example:

```python
arr[0:2, 1:3]
arr[3:6, 3:5]
arr[2:4, 1:4]
```

---

# 8. Boolean Indexing

Filter elements using conditions.

```python
arr[arr % 2 == 0]
arr[arr > 10]
```

---

# 9. Arithmetic Operations

Operations are performed element-wise.

```python
a + b
a - b
a * b
a / b
a // b
a ** b
```

> Arrays must have compatible shapes.

---

# 10. Broadcasting

A scalar automatically operates on every element.

```python
arr + 10
arr * 5
arr / 2
```

Broadcasting also works with compatible array shapes.

---

# 11. Copying Arrays

## Assignment (Reference)

```python
b = a
```

Both variables point to the same array.

---

## Independent Copy

```python
b = a.copy()
```

Changes in `b` do not affect `a`.

---

# 12. Matrix Operations

### Matrix Multiplication

```python
A @ B
np.dot(A, B)
```

### Transpose

```python
A.T
```

---

# 13. Stacking Arrays

## Vertical Stack

```python
np.vstack((a, b))
```

## Horizontal Stack

```python
np.hstack((a, b))
```

## Column Stack

```python
np.column_stack((a, b))
```

---

# 14. Splitting Arrays

## Horizontal Split

```python
np.hsplit(arr, parts)
```

Number of parts must divide the number of columns.

## Vertical Split

```python
np.vsplit(arr, parts)
```

Number of parts must divide the number of rows.

---

# 📌 Key Takeaways

* NumPy arrays are faster and more memory-efficient than Python lists.
* Array operations are vectorized (no explicit loops needed).
* Broadcasting simplifies mathematical operations.
* Use slicing and boolean indexing for efficient data selection.
* Use `.copy()` when an independent copy is required.
* Matrix multiplication uses `@` or `np.dot()`.
* Stacking and splitting are useful for combining and dividing datasets.

# 📖 NumPy Documentation & References

>The official NumPy documentation is the best place to learn about functions, methods, and advanced concepts.

## 🌐 Official Resources

* Official Documentation
* https://numpy.org/doc/stable/

* NumPy User Guide
* https://numpy.org/doc/stable/user/

* NumPy API Reference
* https://numpy.org/doc/stable/reference/

* NumPy Beginner's Guide
* https://numpy.org/doc/stable/user/absolute_beginners.html

* NumPy Tutorials
* https://numpy.org/numpy-tutorials/
