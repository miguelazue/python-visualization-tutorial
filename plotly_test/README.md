# Setup
In this example, we use conda and Python 3. 

## Install Anaconda
Download the 3.7 version of Anaconda from: https://www.anaconda.com/download

Anaconda already [ships with a bunch of packages](https://docs.anaconda.com/anaconda/packages/pkg-docs/), e.g.:
 * ipywidgets
 * jupyter and jupyterlab
 * matplotlib
 * numpy
 * pandas
 * scipy
 * seaborn

But: not plotly.

### Conda Environments
Best practice is to create an environment per project.  
Some commands to manage environments from: https://conda.io/docs/user-guide/tasks/manage-environments.html
```
conda create --name test_env python                 ... create a python environment named test_env
conda create --name jupyter_env jupyterlab python   ... create a python environment named jupyter_env with package jupyterlab
conda create --name va_lab python

conda activate test_env                             ... activate environment test_env
conda env list                                      ... list all environments
conda list                                          ... list all packages available in environment (!= packages shipped with anaconda)
conda install numpy                                 ... install an additional package
conda install --yes --file requirements.txt         ... install packages listed in a requirements file
conda deactivate                                    ... leave conda enviroment
conda env remove --name test_env                    ... remove an environment from disk
```

## Optional: JupyterLab
If you prefer not to use Anaconda, find instructions at: https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html  

### Plotly for Jupyterlab:
You need to install Jupyter Lab extensions to display the widgets. See: https://github.com/plotly/plotly.py#jupyterlab-support-python-35


# Usage
Checkout this repo and change into the folder:
```
git clone https://github.com/keckelt/python-tutorial-VA2018.git
cd python-tutorial-VA2018/
```

Create a new environemnt and install the packages needed in the tutorial:
```
conda create --name python-tutorial python
conda activate python-tutorial
conda install --yes --file requirements.txt 
```


Launch Jupyter :
```
jupyter notebook
```
Jupyter should open a new tab with url http://localhost:8888/lab and display the tutorial files.








Setup Juypter: 

Setup Plotly: https://github.com/plotly/plotly.py#installation
Jupyter Widgets JupyterLab Extension Versions: https://github.com/jupyter-widgets/ipywidgets/tree/master/packages/jupyterlab-manager 

Brushing Example: https://plot.ly/~empet/14975/brushingselected-points-h/#/



Misc: https://jakevdp.github.io/blog/2017/12/05/installing-python-packages-from-jupyter/