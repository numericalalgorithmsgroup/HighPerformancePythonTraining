# High Performance Python
##  Jonathan Boyle - Software Engineer at NAG
* Jonathan.Boyle@nag.co.uk


# Materials & Demos

## Python profiling

* [Introduction to Profiling](./profilers.ipynb) - Measuring where time in spent in Python using `time`, `timeit`, `cprofile`, `line_profile` and `SnakeViz`.

## NumPy

* [An introduction to improving Python performance with Numpy](./numpy.ipynb) - Examples showing where switching to a Numpy version of an algorithm can provide speed-ups compared to pure Python.

### What a difference a BLAS makes

These notebooks demonstrate the importance of using optimised BLAS and LAPACK for any given architecture to get best performance. They compare three implementations of BLAS on the same hardware. 

**In order to repeat this on your own machine, you'll need to install the same BLAS libraries, e.g. using pip or conda in different conda environments.**

* [Summary of Results](./BLAS_LAPACK_results.ipynb)
* [Linear Algebra using Unoptimised BLAS](./numpy_unoptimised_BLAS.ipynb) - Run on a 16 core Azure Instance
* [Linear algebra speed using Intel MKL](./numpy_intelMKL.ipynb) - Run on a 16 core Azure Instance
* [Linear algebra speed using OpenBLAS](./numpy_openBLAS.ipynb) - Run on a 16 core Azure Instance

### Precision and speed

* [Precision and speed demo](./precision_and_speed.ipynb) - Comparision of time to multiply two matrices for different NumPy floating point precisions. 

## Demonstrations using the NAG Library for Python

The [NAG Library for Python](https://www.nag.co.uk/content/nag-library-python) has over 1900 routines covering many areas of applied mathematics, optimisation, statistics and traditional machine learning.  It uses the exact same code for the algorithms as the NAG Library for C, C++ and Fortran.

Many financial institutions have site licenses for NAG products where a typical scenario is to use Python for prototyping and C++ for deployment.  One advantage of using the NAG Library for Python is that you will be using identical implementations of all algorithms in both C++ and Python (and Fortran and MATLAB etc) which can aid in deployment.

**All delegates of this course are entitled to a one-year, free trial for Python, MATLAB, C,C++,Java, .NET and Fortran interfaces to the library for personal use.**  Contact support@nag.co.uk quoting **WBS MLI**.

A large number of examples can be found in the [NAG GitHub repo](https://github.com/numericalalgorithmsgroup/NAGPythonExamples), and the full [NAG Library Manual](https://www.nag.com/numeric/nl/nagdoc_latest/) describes all the available routines, click on **Interface Contents** to see a list of chapters. Here are a few examples. 

* [Comparing SciPy and NAG Library accuracy for Mathieu function characteristic values](https://github.com/numericalalgorithmsgroup/NAGPythonExamples/blob/master/special_functions/mathieu_functions.ipynb) This demo shows an example where **the NAG Library computes the correct values, and SciPy sometimes doesn't**, at least for version 1.6.2 of SciPy.
* [Local optimisation using Second Order Cone Programming](https://github.com/numericalalgorithmsgroup/NAGPythonExamples/tree/master/local_optimization/SOCP) Various Notebooks showing examples of using Second Order Cone Programming, includes Portfolio Optimization examples. 
* [python_3_interface_levels.ipynb](./nag_examples/python_3_interface_levels.ipynb) An in-depth tutorial on the interfaces available in the NAG Library for Python.  Includes demonstrations of solving linear systems that can be **many times faster than the standard Numpy or Scipy solvers** because NAG gives access to many more specialised routines.
* [noisy_polynomial_regression.ipynb](./nag_examples/noisy_polynomial_regression.ipynb) Looks at NAG's **Linear Programming** optimisation solvers compared to those of SciPy when solving a noisy polynomial regression problem.  Also considers the benefit you get when using a completeley tailored algorithm for your problem. **NAG's Linear Programming solvers were found to be faster than the SciPy equivalents for this problem**.
* [Anderson_Acceleration_Poisson.ipynb](https://github.com/numericalalgorithmsgroup/NAGPythonExamples/blob/master/roots/Anderson_Acceleration_Poisson.ipynb) Uses Numba to accelerate each iteration of an iterative solver and then uses NAG's Anderson Acceleration routine to reduce the number of iterations required.

Some of these have been taken from our [NAG Python Examples](https://github.com/numericalalgorithmsgroup/NAGPythonExamples) and [NAG Library for Python Basic Training](https://github.com/numericalalgorithmsgroup/NAGPythonLibraryTraining) GitHub repos.

## Cython

* [Introduction to Cython](./cython.ipynb) - Examples of speed-up after statically compiling Python code with Cython.  

## Numba
* [Introduction to Numba](./numba.ipynb) - Just in Time compilation in Python. Get speeds that are orders of magnitude faster than Pure Python and even Numpy. Includes methods for parallelising certain algorithms.

## Different versions of code and their speed-ups relative to Python

* [Prime Sieve](./solutions/prime_sieve_comparisons.ipynb) - Several versions of the prime sieve algorithm using Pure Python, Numba and Numpy
* [Asian Option Pricing](./solutions/option_pricing_comparison.ipynb) - Up to a 240x speed up from a basic Python implementation

## CuPy

* [CuPy demo](./cupy.ipynb) - compares time for matrix multiplication on a CPU using NumPy and on a GPU using CuPy.  

## What we didn't tell you

This course is evolving and there are several technologies that have not been covered yet. 
Feel free to add requests!



```python

```
