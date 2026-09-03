# ECE-2112-PA-2
**Made by: Sophia Marielle R. Quizon | 2ECE-B**

The content of this repository contains the Programming Assignment for the course Advanced Computer Programming and Algorithms for the S.Y. 2026-2027.

# 1. Reproducible Normalization Problem

The reproducible normalization problem creates a 5 x 5 NumPy array containing random integers from 10 to 100. A fixed random seed is used so that generated values remain the same every time the program is executed. The array is then normalized by subtracting its mean and dividing it by its population standard deviation.

The following methods are used: 

• `np.random.seed(2112)` - Produces the same random numbers every run.

• `np.random.randint()` - Creates a 5 x 5 array of integers.

• `X.mean()` - Calculates the mean of the array.

• `X.std()` - Calculates the standard deviation of the array.

• `X_normalized = (X - X.mean()) / X.std()` - Normalizes each value in the array by subtracting the mean and dividing by the standard deviation.

The combination of the different operations gives the final function:

```python
import numpy as np

np.random.seed(2112)
X = np.random.randint(10, 101, size=(5, 5))

X_normalized = (X - X.mean()) / X.std()
X_normalized

```
# 2. Cubes Divisible by 4 Problem

The cubes divisible by 4 problem creates the first 100 positive integers, cube every element, and reshape the result into a 10 × 10 ndarray. A boolean condition is then applied to extract only the cubed values that are divisible by 4, while keeping the NumPy's row-major order.

The following methods are used: 

• `np.arange (1, 101)` - Creates an array containing integers from 1 to 100.

• `(integers ** 3).reshape (10, 10)` - Cubes every element through exponentiation and rearranges the array into 10 x 10 matrix.

• `div_by_4 = C[C % 4 == 0]` - Uses a boolean indexing that identifies values divisible by 4 and selects only the elements that satisfy the condition.

The combination of the different operations gives the final function:

```python
import numpy as np

integers = np.arange (1, 101)
C = (integers ** 3).reshape (10, 10)

div_by_4 = C[C % 4 == 0]
div_by_4

print (div_by_4)
```

# 3. Above-Mean Squares Problem

The above-mean squares problem creates an array containing the first 36 positive integers and arranges them into a 6 x 6 ndarray. Each value is then squared. The mean of the squared values is calculated, and Boolean filtering is used to select only the values that are greater than the mean.

The following methods are used: 

• `np.arange (1, 37)` - Creates an array containing integers from 1 to 36.

• `integers.reshape (6, 6) ** 2` - Rearranges the array into 6 x 6 matrix and squares every element included in the array.
 
• `S.mean()` - Calculates the mean of all the elements in the squared array.

• `S[S > S_mean]` - Uses a boolean indexing to select only the values that are greater than the calculated mean.

The combination of the different operations gives the final function:

```python
import numpy as np

integers = np.arange (1, 37)
S = integers.reshape (6, 6) ** 2

S_mean = S.mean()
above_mean = S[S > S_mean]
```

Thank you for reading!

For reference of the main python program for Programming Assignment 1, kindly click the link and download:
https://github.com/sphmrlle/ECE-2112-PA-2

### **README file Version History:**

September 1, 2026 - Initial README ouput uploaded and drafted.

September 2, 2026 - Final README updated
