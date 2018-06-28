## Installation Requirements
These files in the Jupyter directory need to be loaded onto your workstation or server where Jupyter notebooks normally run. If you do not have Jupyter installed, there are a number of articles available on the web that tell you how to get it up and running. I've given up a quick write-up below on what you need to do at a minimum to use these notebooks.

### Jupyter
You need to have Jupyter notebook installed on your system, which also needs Python to be installed on your system. If you already have Python available, odds are that you have Jupyter installed as well. The next set of commands will install Python on your platform and then install the Jupyter components.

### Anaconda or Miniconda
Anaconda is an Open Data Science Platform that is powered by Python http://www.continuum.io. The platform keeps track of packages and their dependencies for development with Jupyter notebooks and Python. This makes it very easy to install extensions for Python without having to manually install everything.

Download the Anaconda or Miniconda package applicable to your platform. Miniconda creates the minimal system required for using Python and Jupyter, while Anaconda installs all major packages. There are two versions of Python - V2 or V3. While it doesn't matter which one you use for most notebooks, there are some situations where you may want to use the Python 2 library. 

After installing Anaconda/Miniconda, you should issue the following commands from a shell that will update and install components required by the notebook.

```
conda update conda      - This will update the tool itself so you have the latest code
conda install jupyter   - This will install the jupyter notebook
conda install maplotlib - This library is used for plotting graphs
conda install pandas    - This library allows you to run SQL commands against 
                          a database and display the results
conda update libgcc     - This is the compiler for Python extensions
```

At this point your installation should have Jupyter available on your system. To start the notebook server you need to issue the following command:
```
jupyter notebook (opens browser)
jupyter notebook --no-browser (runs as a service)
```
The first command will open up a browser window that displays your notebooks. You can click on one of these notebooks to see the contents. If no notebooks are available, you will need to move the files in the Github jupyter directory to a local folder on your system that the program can access.

### Db2 Extensions with RESTful APIs

To create a connection to Db2 with the Python Db2 extensions you must run the `db2re.ipynb` notebook from within your Jupyter Notebook. This will load the required libraries for communicating with Db2 using RESTful API calls. There is no need to install a Db2 driver when using these RESTful APIs. Only Db2 on Cloud is supported with this package. To use Db2 on Docker, or natively on an operating system, please refer to the Db2 Jupyter Notebook libraries instead.
