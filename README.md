# SRE (Under Development)
Sequential Regression Extrapolation (SRE): A method of extrapolation with machine learning and regression algorithms.

## To Use:
1. Clone Directory
2. At the top of any file using these codes, have the code:
```python
from Analyis import *
from Extrapolate import *
from Regression import *
from Support import *
```
* Current version of the code must be used from the directory that contains the files.
* See StartHere.ipynb for simple test cases to use as beginning examples.

## File Outline

#### **Analysis.py**
Contains classes VisualAnalysis and ErrorAnalysis.  Perform graphical and numerical analysis on the results from SRE analysis.
#### **Extrapolate.py**
Contains two functions: sequential_extrapolate extrapolates a one dimensional data set and sequential_column_extrapolate extrapolates a matrix row by row
#### **Regression.py**
Contains the parent class Regression, and then the child classes LiR (Linear Regression), RR (Ridge Regression), and KRR (Kernel Ridge Regression).  Performs close form linear, ridge, and kernel ridge regression on a given data set.
#### **Support.py**
Contains supporting functions including format_sequential_data, to get a data series into sequential data format.
#### **DataSets.py**
A collection of data sets (mostly physics related) for testing the codes
#### **StartHere.ipynb**
A notebook showcasing simple use cases of the SRE library for extrapolation.

## Brief Overview of the Regression Algorithms

## Sequential Data Formatting
