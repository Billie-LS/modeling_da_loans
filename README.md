# **Columbia University Engineering, New York FinTech Bootcamp** 
# **August 2022 Cohort**
![image1](images/image1.png)
## *Project 2 - LendingGenie*

Scenario - Credit risk analysis and loan grant decision are two of the most important operations for financial institutions. By leveraging the extensive large data of historical loans performance, we need to train a model to accurately predict future outcomes.

Objective - Using historical large data, employ supervised machine learning model optimization to anlayze the features of potential borrowers in order to better predict risk level; i.e. will loan be paid back in full vs default and/or written off.  Given the large data available with extensive features, the model should be able to more accurately and efficiently provide predictions using more than traditional credit reports and limited features.  

Product - 

>* Our product is a cloud-based lending-as-a-service (LaaS) solution that can be offered to financial institutions as an API.
>* The product uses Python-libraries including pandas and sci-kit learn, among others, to clean, process, and fit models based on the desired risk parameters to accurately predict customers fit for lending opportunities. 
>* The product is deployed using Amazon Web Services (AWS). Specifically, SageMaker in order for clients to be able to run the model on the cloud. 
___

### **Train (75%) and Test (25%) Summary Analysis**

>* Excluding the target/'labels' column, raw data provided 150 features. After preprocessing, data clean up, and preparation features count reduced to 110.
>* Following use of StandardScaler with Principal Component Analysis (PCA), total features reduced to 61 with 95% explained variance ratio.

Following is the summary of results:

![results](images/results.png)
___

### **Metrics for trained models applied to alternate/virgin dataset, i.e. 'bank2'**

>* Excluding the target/'labels' column, raw data provided 150 features. After preprocessing, data clean up, and preparation features count reduced to 110.
>* Following use of StandardScaler with Principal Component Analysis (PCA), total features reduced to 61 with 95% explained variance ratio.

RandomUnderSampler, StandardScaler, PCA, LinearSVC classifier model:

![results](images/image2.png)

StandardScaler, PCA, LinearSVC classifier model:

![results](images/image3.png)

StandardScaler, PCA, LogisticRegression model:

![results](images/image4.png)

StandardScaler, PCA, hyupertuning XGBClassifier model:

![results](images/image5.png)
___

## **Technologies**
___


### **Dependencies**

This project leverages Jupyter Lab v3.4.4 and Python version 3.9.13 packaged by conda-forge | (main, May 27 2022, 17:01:00) with the following packages:


* [sys](https://docs.python.org/3/library/sys.html) - module provides access to some variables used or maintained by the interpreter and to functions that interact strongly with the interpreter.

* [os](https://docs.python.org/3/library/os.html) - module provides a portable way of using operating system dependent functionality.

* [opendatasets](https://pypi.org/project/opendatasets/0.0.103/) - module is a Python library for downloading datasets from online sources like Kaggle and Google Drive using a simple Python command.

* [NumPy](https://numpy.org/doc/stable/user/absolute_beginners.html) - an open source Python library used for working with arrays, contains multidimensional array and matrix data structures with functions for working in domain of linear algebra, fourier transform, and matrices.

* [pandas](https://pandas.pydata.org/docs/) - software library written for the python programming language for data manipulation and analysis.

* [Scikit-learn](https://scikit-learn.org/stable/getting_started.html) - an open source machine learning library that supports supervised and unsupervised learning; provides various tools for model fitting, data preprocessing, model selection, model evaluation, and many other utilities.

* [Path](https://pandas.pydata.org/docs/reference/api/pandas.concat.html) - from pathlib - Object-oriented filesystem paths, Path instantiates a concrete path for the platform the code is running on.

* [DateOffset](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.tseries.offsets.DateOffset.html) - from pandas - sttandard kind of date increment used for a date range.

* [confusion_matrix](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.confusion_matrix.html) - from sklearn.metrics, computes confusion matrix to evaluate the accuracy of a classification; confusion matrix *C* is such that *Cij* is equal to the number of observations known to be in group *i* and predicted to be in group *j*.

* [balanced_accuracy_score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.balanced_accuracy_score.html) - from sklearn.metrics, compute the balanced accuracy in binary and multiclass classification problems to deal with imbalanced datasets; defined as the average of recall obtained on each class.

* [f1_score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.f1_score.html) - from sklearn.metrics, computes the F1 score, also known as balanced F-score or F-measure; can be interpreted as a harmonic mean of the precision and recall, where an F1 score reaches its best value at 1 and worst score at 0.

* [classification_report_imbalanced](https://glemaitre.github.io/imbalanced-learn/generated/imblearn.metrics.classification_report_imbalanced.html) - from imblearn.metrics, compiles the metrics: precision/recall/specificity, geometric mean, and index balanced accuracy of the geometric mean.

* [SVMs](https://scikit-learn.org/stable/modules/svm.html) - from scikit-learn, support vector machines (SVMs) are a set of supervised learning methods used for classification, regression and outliers detection.

* [LogisticRegression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html) - from sklearn.linear_model, a Logistic Regression (aka logit, MaxEnt) classifier; implements regularized logistic regression using the ???liblinear??? library, ???newton-cg???, ???sag???, ???saga??? and ???lbfgs??? solvers - regularization is applied by default.

* [AdaBoostClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.AdaBoostClassifier.html) - from sklearn.ensemble, a meta-estimator that begins by fitting a classifier on the original dataset and then fits additional copies of the classifier on the same dataset but where the weights of incorrectly classified instances are adjusted such that subsequent classifiers focus more on difficult cases.

* [KNeighborsClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html) - from sklearn.neighbors, a classifier implementing the k-nearest neighbors vote.

* [StandardScaler](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html) - from sklearn.preprocessing, standardize features by removing the mean and scaling to unit variance.

* [hvplot](https://hvplot.holoviz.org/getting_started/hvplot.html) - provides a high-level plotting API built on HoloViews that provides a general and consistent API for plotting data into numerous formats listed within linked documentation.

* [matplotlib.pyplot](https://matplotlib.org/3.5.3/api/_as_gen/matplotlib.pyplot.html) a state-based interface to matplotlib. It provides an implicit, MATLAB-like, way of plotting. It also opens figures on your screen, and acts as the figure GUI manager

* [Seaborn](https://seaborn.pydata.org/tutorial/introduction) a library for making statistical graphics in Python. It builds on top of matplotlib and integrates closely with pandas data structures.

* [pickle](https://docs.python.org/3/library/pickle.html) Python object serialization; module implements binary protocols for serializing and de-serializing a Python object structure. ???Pickling??? is the process whereby a Python object hierarchy is converted into a byte stream, and ???unpickling??? is the inverse operation.

* [joblib.dump](https://joblib.readthedocs.io/en/latest/generated/joblib.dump.html) Persist an arbitrary Python object into one file.

___

### **Hardware used for development**

MacBook Pro (16-inch, 2021)

    Chip Appple M1 Max
    macOS Venture version 13.0.1

### **Development Software**

Homebrew 3.6.11

    Homebrew/homebrew-core (git revision 01c7234a8be; last commit 2022-11-15)
    Homebrew/homebrew-cask (git revision b177dd4992; last commit 2022-11-15)

Python Platform: macOS-13.0.1-arm64-arm-64bit

    Python version 3.9.15 packaged by conda-forge | (main, Nov 22 2022, 08:52:10)
    Scikit-Learn 1.1.3
    pandas 1.5.1
    Numpy 1.21.5

pip 22.3 from /opt/anaconda3/lib/python3.9/site-packages/pip (python 3.9)


git version 2.37.2

---
## *Installation of application (i.e. github clone)*

In the terminal, navigate to directory where you want to install this application from the repository and enter the following command

```python
git clone git@github.com:prpercy/LendingGenie.git
```

You will require Kaggle API credentials to run the jupyter lab notebook.

How to Use Kaggle - Public API
[Kaggle](https://www.kaggle.com/docs/api)

Kaggle - opendatasets
[Kaggle](https://pypi.org/project/opendatasets/)

```python
> pip install opendatasets --upgrade

```

```python
> pip install kaggle

```

```python
> git lfs install

```
In order to use the Kaggle???s public API, you must first authenticate using an API token. From the site header, click on your user profile picture, then on ???My Account??? from the dropdown menu. This will take you to your account settings at [KaggleAccount](https://www.kaggle.com/account). Scroll down to the section of the page labelled API:

To create a new token, click on the ???Create New API Token??? button. This will download a fresh authentication token onto your machine.

Once you obtain your Kaggle credentials and download the associated 'kaggle.json', proceed to usage below.

---
## **Usage**

From terminal, the installed application is run through jupyter lab web-based interactive development environment (IDE) interface by typing at prompt:

```python
> jupyter lab

```
The file you will run is:

```python
lending_genie.ipynb

```
Once it starts to run, you will be asked to enter your credentials-

![Credentials](images/request_credentials.png)


If running the code generates error:
```python
FileExistsError: [Errno 17] File exists: 'models_trained'
```
You will need to delete directory 'models_trained'
___

## **Version control**

Version control can be reviewed at:

```python
https://github.com/prpercy/LendingGenie
```

[repository](https://github.com/prpercy/LendingGenie)


___
![contribute1](images/contribute1.png)

### **Authors**

Conyea, Will
    [LinkedIn]()
    [@GitHub](https://github.com/willco-1)

Lopez, Esteban
    [LinkedIn](https://www.linkedin.com/in/estebandlopez/)
    [@GitHub](https://github.com/Esteban-D-Lopez)

Mandal, Dinesh
    [LinkedIn](https://www.linkedin.com/in/dineshmandal/)
    [@GitHub](https://github.com/dinesh-m)
    
Patil, Pravin
    [LinkedIn](https://www.linkedin.com/in/pravin-patil-5880301)
    [@GitHub](https://github.com/prpercy)

Loki 'billie' Skylizard
    [LinkedIn](https://www.linkedin.com/in/l-s-6a0316244)
    [@GitHub](https://github.com/Billie-LS)


Additions
![contribute1](images/contribute2.png)
Commits
![contribute3](images/contribute3.png)
### **BootCamp lead instructor**

Vinicio De Sola
    [LinkedIn](https://www.linkedin.com/in/vinicio-desola-jr86/)
    [@GitHub](https://github.com/penpen86)


### **BootCamp teaching assistant**

Santiago Pedemonte
    [LinkedIn](https://www.linkedin.com/in/s-pedemonte/)
    [@GitHub](https://github.com/Santiago-Pedemonte)

___

### **Additional references and or resources utilized**

EDA ??? Exploratory Data Analysis
[SearchMedium](https://medium.com/analytics-vidhya/eda-exploratory-data-analysis-d0fb1fd40cb9)

splitting data
[MungingData](https://mungingdata.com/python/split-csv-write-chunk-pandas/)

dealing with compression = gzip
[Stack Overflow](https://stackoverflow.com/questions/44659851/unicodedecodeerror-utf-8-codec-cant-decode-byte-0x8b-in-position-1-invalid)

numeric only corr()
[Stack Overflow](https://stackoverflow.com/questions/74305444/error-while-trying-to-run-corr-in-python-with-pandas-module)

find NaN
[Stack Overflow](https://stackoverflow.com/questions/29530232/how-to-check-if-any-value-is-nan-in-a-pandas-dataframe)

color palette
[seaborn](https://seaborn.pydata.org/tutorial/color_palettes.html)

horizontal bar graph
[seaborn](https://hvplot.holoviz.org/reference/pandas/barh.html)

dataframe columns list
[geeksforgeeks](https://www.geeksforgeeks.org/how-to-get-column-names-in-pandas-dataframe/)

dataframe drop duplicates
[geeksforgeeks](https://www.geeksforgeeks.org/python-pandas-dataframe-drop_duplicates/)

PCA?????????how to choose the number of components
[mikulskibartosz](https://www.mikulskibartosz.name/pca-how-to-choose-the-number-of-components/)

LinearSVC classifier
[DataTechNotes](https://www.datatechnotes.com/2020/07/classification-example-with-linearsvm-in-python.html)

In Depth: Parameter tuning for SVC
[All things AI](https://medium.com/all-things-ai/in-depth-parameter-tuning-for-svc-758215394769)

ConvergenceWarning: Liblinear failed to converge
[Stack Overflow](https://stackoverflow.com/questions/52670012/convergencewarning-liblinear-failed-to-converge-increase-the-number-of-iterati)

Measure runtime of a Jupyter Notebook code cell
[Stack Overflow](https://stackoverflow.com/questions/43307653/measure-runtime-of-a-jupyter-notebook-code-cell)

Building a Machine Learning Model in Python
[Frank Andrade](https://towardsdatascience.com/a-beginners-guide-to-text-classification-with-scikit-learn-632357e16f3a)

KNeighborsClassifier()
[scikit-learn](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html#sklearn.neighbors.KNeighborsClassifier)

Linear Models
[scikit-learn](https://scikit-learn.org/stable/modules/linear_model.html#logistic-regression)

LogisticRegression()
[scikit-learn](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)

Classifier comparison
[scikit-learn](https://scikit-learn.org/stable/auto_examples/classification/plot_classifier_comparison.html)

XGB Classifier
[AnalyticsVidhya](https://www.analyticsvidhya.com/blog/2016/03/complete-guide-parameter-tuning-xgboost-with-codes-python/)

Install XGBoost
[dmlc_XGBoost](https://xgboost.readthedocs.io/en/stable/install.html)

XGBoost
[dmlc_XGBoost](https://xgboost.readthedocs.io/en/stable/python/python_api.html)

XGBoost
[towardsdatascience](https://towardsdatascience.com/getting-started-with-xgboost-in-scikit-learn-f69f5f470a97)

Using XGBoost in Python Tutorial
[datacamp](https://www.datacamp.com/tutorial/xgboost-in-python)

Kaggle - XGBoost classifier and hyperparameter tuning 85%
[Kaggle](https://www.kaggle.com/code/michalbrezk/xgboost-classifier-and-hyperparameter-tuning-85)

How to Best Tune Multithreading Support for XGBoost in Python
[machinelearningmastery](https://machinelearningmastery.com/best-tune-multithreading-support-xgboost-python/)

AttributeError: 'GridSearchCV' object has no attribute 'grid_scores_'
[csdn.net](https://blog.csdn.net/weixin_44025103/article/details/125561477)

How to check models AUC score
[projectpro](https://www.projectpro.io/recipes/check-models-auc-score-using-cross-validation-in-python)

Git Large File Storage
[git_lfs](https://git-lfs.github.com/)

git lfs is not a command Mac OS
[Stack Overflow](https://stackoverflow.com/questions/58796472/git-lfs-is-not-a-command-mac-os)

Histograms and Skewed Data
[Winder](https://winder.ai/histograms-and-skewed-data/)

Creating Histograms using Pandas
[Mode](https://mode.com/example-gallery/python_histogram/)

Credit Risk Modelling [EDA & Classification]
[RStudio](https://rpubs.com/nonebean/566793)



Save and Load Machine Learning Models in Python with scikit-learn
[machinelearningmastery](https://machinelearningmastery.com/save-load-machine-learning-models-python-scikit-learn/)

Quick Hacks To Save Machine Learning Model using Pickle and Joblib
[AnalyticsVidhya](https://www.analyticsvidhya.com/blog/2021/08/quick-hacks-to-save-machine-learning-model-using-pickle-and-joblib/)





Kaggle - Lending Club data
[Kaggle](https://www.kaggle.com/datasets/wordsforthewise/lending-club)

Kaggle - Lending Club defaulters predictions
[Kaggle](https://www.kaggle.com/code/faressayah/lending-club-loan-defaulters-prediction)

Kaggle - Lending Club categorical features analysis
[Stack Overflow](https://www.kaggle.com/code/mariiagusarova/categorical-features-analysis-on-loan-fintech-data)


___
## **License**

MIT License

Copyright (c) [2022] [Will Conyea, Esteban Lopez, Dinesh Mandal, Pravin Patil, Loki 'billie' Skylizard]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.



