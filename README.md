# Usage
## MyBinder
Go to: https://mybinder.org/v2/gh/JKU-ICG/python-visualization-tutorial/master
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/JKU-ICG/python-visualization-tutorial/master)

MyBinder installs the dependencies specified inside of the `requirements.txt` for you.


## Locally
### Setup
In this example, we use Anaconda and Python 3. 

#### Install Anaconda
Download the 3.7 version of Anaconda from: https://www.anaconda.com/download

Anaconda is a package distribution that contains the *Conda* package manager, but also a bunch of [other frequently used packages](https://docs.anaconda.com/anaconda/packages/pkg-docs/), e.g.:
 * ipywidgets
 * jupyter and jupyterlab
 * matplotlib
 * numpy
 * pandas
 * scipy
 * seaborn

But: not plotly, we will install it later.

**Conda Environments**  
Best practice is to create an environment per project.  
Some commands to manage environments from: https://conda.io/docs/user-guide/tasks/manage-environments.html
```
conda create --name test_env python                 ... create a python environment named test_env
conda create --name jupyter_env jupyter python   ... create a python environment named jupyter_env with package jupyter

conda activate test_env                             ... activate environment test_env
conda env list                                      ... list all environments
conda list                                          ... list all packages available in environment (!= packages shipped with anaconda)
conda install numpy                                 ... install an additional package
conda install --yes --file requirements.txt         ... install packages listed in a requirements file
python -m pip install <package>                     ... install a package not aviailable via conda, also see (†)
conda deactivate                                    ... leave conda enviroment
conda env remove --name test_env                    ... remove an environment from disk
```

† See this article on [why you should prefer `python -m pip` over `pip`](https://snarky.ca/why-you-should-use-python-m-pip/).

### Start
Checkout this repo and change into the folder:
```
git clone https://github.com/JKU-ICG/python-visualization-tutorial.git
cd python-visualization-tutorial/
```

Create a new environemnt and install the packages needed in the tutorial:
```
conda create --name python-tutorial python
conda activate python-tutorial
conda install -c conda-forge  --yes --file requirements.txt 
```


Launch Jupyter :
```
jupyter notebook
```
Jupyter should open a new tab with url http://localhost:8888/ and display the tutorial files.
