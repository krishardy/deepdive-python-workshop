Deep Dive Alumni Python Workshop (Dec 2nd, 2017)
===

Prework
---

Download and install Anaconda w/ Python 3.6

[Anaconda Downloader](https://www.anaconda.com/download/#linux)

Download the Anaconda Cheat Sheet in case you need it.  It has some tips for working with Anaconda, but we hopefully won't need it.

[Anaconda Cheatsheet](https://docs.anaconda.com/_downloads/Anaconda_CheatSheet.pdf)

[Conda Package Manager Cheatsheet](https://conda.io/docs/user-guide/cheatsheet.html)

Keep this url handy.  You may need it.  [Python Standard Library Documenation](https://docs.python.org/3.6/library/index.html)


Plan
---

Kris will be presenting an introduction on Python, using [Learnpython.org](http://www.learnpython.org) as the lesson template.

We will then do an intro to Machine Learning, focusing primarily on decision trees and hopefully a little time to talk about neural networks.  The focus will be focused on understanding how some ML algorithms work, and how to use the Scikit Learn library.

We will be going through the [Intro to Machine Learning](http://scikit-learn.org/stable/tutorial/basic/tutorial.html),
[Decision Trees](http://scikit-learn.org/stable/modules/tree.html) using Scikit Learn,
and hopefully start in on [Neural Networks](http://scikit-learn.org/stable/modules/neural_networks_supervised.html) using Skikit Learn. 

The Pandas tutorial is here: [10 Minutes to pandas](http://pandas.pydata.org/pandas-docs/stable/10min.html#min)


Intro to Python
---

Topics:

- Hello, World!
 - Create in text editor
 - Running from IDE (spyder) & shell
 
- Variables & Common types
 - Numeric (int, float)
 - Strings
 - Lists
 - Tuple (immutable list)
 - Dictionaries
 - Exceptions

- Basic operations (math, methods, documentation)
 - Math (add, subtract, multilpy, divide)
 - Exponential (2 ** 4 == 16)
 - Python documentation is at python.org

- Lists (referencing elements, setting values, iteration)
 - Referencing elements
   - First, last, slicing
 - Setting values
 - Push
 - Pop
 - Iteration
 - Math
 
- Strings
 - % syntax
 - String.format syntax
 - character references
 - slicing
 - counting
 - index
 
- dict
 - initializing
 - referencing values
 - adding values
 - deleting values
 - .get()
 
- Conditions
 - if
   - and
   - or
 - value in list
 
- loops
 - for
  - by element on list / tuple
  - by index on list / tuple (range)
  - by key, value pair in dict
  - by key in dict
 - while
 - break/continue
 - for/else (only break avoids running code in else block)
 
- functions
 - formatting
 - calling functions
 - parameters
 - parameters w/ defaults
 - *args
 - **kwargs
 
- classes
 - methods
 - self
 - attributes
   - static
   - instance

- Exception handling
 - try/except/finally
   
- modules/packages
 - import requests; requests.get("http://www.google.com")
 - creating a module: hello_world (create __init__.py, add run() to __init__.py;
  - in your code, import hello_world; hello_world.run())
 

Pandas
---

- Load data from file
- Showing data
- Select data by row
- Select data by column
- Select only certain rows
- Referencing a single cell
- Doing math on columns
- Filtering rows based on values
- Grouping rows together and calculating statistics
 - also df.groupby(col, as_index=False).agg({'col to aggregate': ['mean', 'std']})
- Plotting

ML
---

- Objective - Knowing the input data and an output (think a point in n-dimensional space (x1,...,xn,y)), can we tune the coefficients of an equation to find the best fit?
 - Linear regression is one example of machine learning
- Supervised learning (classification, regression)
 - TODO: Find good example diagram
- Unsupervised learning (clustering, density estimation, etc.)
 - TODO: Find good example diagram
- Reinforcement learning (reward maximization)
 - TODO: Find good example diagram

Supervised Learning: Decision Trees
---

- TODO: Show diagram
- Talk about theory
 - Algorithm chooses a parameter which gives it the highest information gain (effectively splits the classes)
 - Each value is further tested
- Training vs Validation vs Testing
 - 3 datasets
  - Training - Labeled data
  - Validation - Often 30% of the training data, but could be more or less.  Dataset where the labels have been masked/removed, and you compare the results against the known labels.
  - Testing - Unlabeled data that you want to classify
 - Training is computationally intensive to find the ideal tree
 - Tree can cause overfitting (all values are perfectly matched against the training set, but noise wasn't considered)
- Load dataset and talk about it
 - We have a dataset which shows the known cases of some disease (determined from medical records), plus many people who don't have the disease
- Visualizing the data (matplotlib)
- Asking a question of the data
 - If we have this "inexpensive" data, can we predict who is most likely to have the disease?
- Fitting the data to the training data
- Visualize tree
- Validate validation data
- Tuning parameters (max depth, pruning)
- Predict classification of test data

Neural Networks
---

- Talk about how Neural Networks work
 - Input
 - Perceptrons
  - Weights
 - Outputs
 - Backpropagation
- Using the same dataset, use the MLP Classifier to classify the data