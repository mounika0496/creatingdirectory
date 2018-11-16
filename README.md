# Creating Directory

This repository that contains the code for Creating a directory

### Table of Contents
* [Getting Started](#getting-started)
* [Prerequisites](#prerequisites)
* [Installing](#installing)
* [Python code for Creating Directory](#python-code-for-creating-directory)
* [Approach Towards The Development of Code](#approach-towards-the-development-of-code)
* [Built With](#built-with)
* [Author](#author)

## Getting Started

These instruction will get you a copy of the project up and running on your local machine for development and testing purposes. 

### Prerequisites
* [Python Text editor](https://www.python.org)

If you donot have python text editor ,you can install anaconda In anaconda you have two types of text editors Jupyter Notebook and Spyder

* [Ananconda cloud](https://anaconda.org)

Jupyter Notebook can be installed  without downloading anaconda by using pip

```pip install jupyternotebook```

### Installing
* After downloading install the binaries
* Then add python to system environment variables
* Then install pip
* Using pip install virtualenv(optional)

### Python code for Creating Directory
```
import os,sys
directory=str(sys.argv[1])
def createFolder(directory):
    try:
        if not os.path.exists(directory):
            os.makedirs(directory)
    except OSError:
        return 'Error:Creating directory'+directory
    else:
        print([os.path.join(directory,f) for f in os.listdir(directory)])

createFolder(directory)
```
### Approach Towards The Development of Code

**PROBLEM OF CREATING DIRECTORY**

1. If we want to create a folder with name which is already existed.
2. While creating directory the input path is wrong it given an OSError.
3. If the folder is already existed then how to the sub-directories.

**APPROACH TOWARDS THE PROBLEMS**

1. Creating a directory  by using if clause.
2. _**if not**_ block executes if the directory is not existed already.
3. If the given input path is wrong then by using try block we can except the error.
4. If the given input folder already existed then to print the paths of sub-directories(using list comprehension).

### Built With
* [Python Text editor](https://www.python.org)

### Author
Mounika Mandha

## Thank You
