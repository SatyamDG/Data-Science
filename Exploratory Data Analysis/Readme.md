# EDA [Exploratory Data Analysis]

* Exploratory Data Analysis (EDA) indeed is the first and one of the most important steps for all the data scientists.Exploratory Data Analysis (EDA) indeed is the first and one of the most important steps for all the data scientists.

* It is quite hard to imagine a model without EDA. Firstly, I would like to give a single line understanding of what EDA is. EDA gives us more insight into the data such as missing values, duplicates, count, mean, median, quantiles, distribution of data, correlation of variables with each other, type, etc. 

* Well, we already have many good packages such as describe(), info(), isnull(), etc, which gives a neat analysis of our data. This sometimes might get us into too much of coding and is time taking, too.

 * A question might arise- “Don’t we have a better and faster way for EDA in a very short time?” And the answer is- “Yes, we do.” There is a package called ‘Pandas Profiling’ with which we can have much analysis with just a single line code. It returns a report in the interactive HTML format which is quite easy to access and analyze the data.


# Installation of Pandas Profiling:
#### Installation with the pip package
*  pip install pandas-profiling
#### Installation with the conda package
* conda install -c conda-forge pandas-profiling

# Jupyter Notebook

* We recommend generating reports interactively by using the Jupyter notebook.

* Start by loading in your pandas DataFrame, e.g. by using


 **import numpy as np**
 **import pandas as pd
 import pandas_profiling**


 **df = pd.DataFrame(
    np.random.rand(100, 5),
    columns=['a', 'b', 'c', 'd', 'e']
)**


* To display the report in a Jupyter notebook, run:

 **df.profile_report(style={'full_width':True})**
 
 
* To retrieve the list of variables which are rejected due to high correlation:

 **profile = df.profile_report()
rejected_variables = profile.get_rejected_variables(threshold=0.9)**


* If you want to generate a HTML report file, save the ProfileReport to an object and use the to_file() function:

 **profile = df.profile_report(title='Pandas Profiling Report')
profile.to_file(output_file="output.html")**
