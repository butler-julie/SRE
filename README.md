# Sequential Regression Extrapolation (SRE) (Under Development)

Sequential Regression Extrapolation (SRE) is a series of Python files that allows for data to be accurately extrapolated using the machine learning algorithms linear regression, ridge regression, and kernel ridge regression as well as a data formatting style called sequential data formatting (described below).  Though machine learning is not typically used for extrapolations, combining the regression algorithms with sequential data formatting enables the machine learning algorithms to learn long term behavior in the data and thus accurately make predictions far outside of its training range.  

## Sequential Data Formatting

SRE also makes use of a method of data formatting called time-series formatting, which is often seen in time-series machine learning applications and recurrent neural networks.  In time-series data formatting, instead of feeding a machine learning algorithm data points of the form (t1, y1), (t2, y2), (t3, y3), etc (where t1, t2, t3 are ordered by time), time series formatting insteads formats the data such that each data point as the following form: ((y1, y2, ...., yn) yn+1) where y1, y2, etc come from time ordered data points and n is a hyperparameter known as the length of the sequence.  n can be any integer greater than one.  The larger n is, the better the machine learning algorithm can learn the time series pattern, but the less points in the formatted data series.  Since not all applications of these codes deal with time ordered data, this method of data formatting will instead be refered to as sequential data formatting, where the data set is ordered based on some x data set.

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
Contains the parent class Regression, and then the child classes LiR (Linear Regression), RR (Ridge Regression), and KRR (Kernel Ridge Regression).  Performs close form linear, ridge, and kernel ridge regression on a given data set.  Since the closed form solutions involve taking the inverse of a matrix, there is a potential for a singularity error.
#### **Support.py**
Contains supporting functions including format_sequential_data, to get a data series into sequential data formatting.
#### **DataSets.py**
A collection of small physics data sets for testing and development.  Note that even though all of these data sets are very small in machine learning terms (each is around 20 data points), SRE is still able to make physically relevant and accurate extrapolations!
#### **StartHere.ipynb**
A notebook showcasing simple use cases of the SRE library for extrapolation.

