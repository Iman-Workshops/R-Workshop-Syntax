## Running R on Colab

There are two main ways to run R on Colab:

**Option 1: Using the R kernel**

1. Open a new Colab notebook.
2. Go to **Runtime > Change runtime type** in the top menu bar.
3. Select **R** from the available runtime options.

Once you've selected the R kernel, you can write and execute R code directly in the notebook cells.

**Option 2: Using the rpy2 package**

If you want to run R code within a Python Colab notebook, you can use the `rpy2` package. Follow these steps:

1. Open a new Python Colab notebook.
2. Install the `rpy2` package using the following command:

```python
!pip install rpy2
```

Use code with caution. Learn more
Import the rpy2 package using the following command:
Python
import rpy2.r as R


Now, you can run R code within Python code cells using the `%%R` magic. For example, the following code will print the value of the variable `x`:

```python
%%R
x <- 2 + 3
print(x)
```

You can also run multiple lines of R code in a cell by starting the cell with `%%R`. For example, the following code will create a vector of numbers and then print the vector:

```python
%%R
x <- c(1, 2, 3, 4, 5)
print(x)
```