# Data Analysis

## JupyterLab

* JupyterLab enables you to work with documents and activities such as Jupyter notebooks, text editors, terminals, and custom components in a flexible, integrated, and extensible manner.

* JupyterLab also offers a unified model for viewing and handling data formats. JupyterLab understands many file formats (images, CSV, JSON, Markdown, PDF, Vega, Vega-Lite, etc.) and can also display rich kernel output in these formats 

* Documents and activities integrate with each other, enabling new workflows for interactive computing, for example:

1- Code Consoles provide transient scratchpads for running code interactively, with full support for rich output.

2- Kernel-backed documents enable code in any text file (Markdown, Python, R, LaTeX, etc.) to be run interactively in any Jupyter kernel.

3 Notebook cell outputs can be mirrored into their own tab, side by side with the notebook, enabling simple dashboards with interactive controls backed by a kernel.

4- Multiple views of documents with different editors or viewers enable live editing of documents reflected in other viewers.

## NumPy Tutorial: Data Analysis with Python

* NumPy is a commonly used Python data analysis package. By using NumPy, you can speed up your workflow, and interface with other packages in the Python ecosystem, like scikit-learn, that use NumPy under the hood. NumPy was originally developed in the mid 2000s, and arose from an even older package called Numeric.

*  csv package :We can read in the file using the csv.reader object, which will allow us to read in and split up all the content from the ssv file.

import csv
with open('winequality-red.csv', 'r') as f:
    wines = list(csv.reader(f, delimiter=';'))

    output :

    [['fixed acidity', 'volatile acidity', 'citric acid', 'residual sugar', 'chlorides', 'free sulfur dioxide', 'total sulfur dioxide', 'density', 'pH', 'sulphates', 'alcohol', 'quality'], ['7.4', '0.7', '0', '1.9', '0.076', '11', '34', '0.9978', '3.51', '0.56', '9.4', '5'], ['7.8', '0.88', '0', '2.6', '0.098', '25', '67', '0.9968', '3.2', '0.68', '9.8', '5']]

## Creating A NumPy Array

We can create a NumPy array using the numpy.array function. If we pass in a list of lists, it will automatically create a NumPy array with the same number of rows and columns.

import csv
with open("winequality-red.csv", 'r') as f:
    wines = list(csv.reader(f, delimiter=";"))
import numpy as np
wines = np.array(wines[1:], dtype=np.float)

output :
 array([[ 7.4 , 0.7 , 0. , ..., 0.56 , 9.4 , 5. ],
[ 7.8 , 0.88 , 0. , ..., 0.68 , 9.8 , 5. ],
[ 7.8 , 0.76 , 0.04 , ..., 0.65 , 9.8 , 5. ],
...,
[ 6.3 , 0.51 , 0.13 , ..., 0.75 , 11. , 6. ],
[ 5.9 , 0.645, 0.12 , ..., 0.71 , 10.2 , 5. ],
[ 6. , 0.31 , 0.47 , ..., 0.66 , 11. , 6. ]])

### NumPy Array Operations

* NumPy makes it simple to perform mathematical operations on arrays. This is one of the primary advantages of NumPy, and makes it quite easy to do computations.

* Single Array Math
If you do any of the basic mathematical operations (/, *, -, +, ^) with an array and a value, it will apply the operation to each of the elements in the array.

wines[:,11] + 10

output: 
array([ 15., 15., 15., ..., 16., 15., 16.])

* Multiple Array Math
It’s also possible to do mathematical operations between arrays. This will apply the operation to pairs of elements. For example, if we add the quality column to itself, here’s what we get:

wines[:,11] + wines[:,11]

output :
array([ 10., 10., 10., ..., 12., 10., 12.])

## Broadcasting 

Unless the arrays that you’re operating on are the exact same size, it’s not possible to do elementwise operations.


## NumPy Array Comparisons

* NumPy makes it possible to test to see if rows match certain values using mathematical comparison operations like <, >, >=, <=, and ==. For example, if we want to see which wines have a quality rating higher than 5, we can do this:

wines[:,11] > 5

output :
array([False, False, False, ..., True, False, True], dtype=bool)

## Combining NumPy Arrays

* With NumPy, it’s very common to combine multiple arrays into a single unified array. We can use numpy.vstack to vertically stack multiple arrays.

white_wines = np.genfromtxt("winequality-white.csv", delimiter=";", skip_header=1)

output: 

(4898, 12)
