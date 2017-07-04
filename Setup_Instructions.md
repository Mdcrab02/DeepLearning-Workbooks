# Configure and Manage Your Environment with Anaconda

Per the Anaconda [docs](http://conda.pydata.org/docs):

> Conda is an open source package management system and environment management system
for installing multiple versions of software packages and their dependencies and
switching easily between them. It works on Linux, OS X and Windows, and was created
for Python programs but can package and distribute any software.

## Overview
These instructions consists of the following:

1. Install [`Anaconda`](https://www.continuum.io/downloads) on your computer
2. Install Github
2. Create a new `conda` [environment](https://conda.io/docs/using/envs.html) using this project
3. Each time you wish to work, activate your `conda` environment

---

## Anaconda Installation

**Download** the version of `Anaconda` that matches your system from [here](https://www.continuum.io/downloads#windows). Make sure you download the version for Python 3.5.

If you're using Mac or Linux, then install [miniconda](http://conda.pydata.org/miniconda.html) on your machine.

**Install Anaconda** Detailed installation instructions below:
- **Linux:** http://conda.pydata.org/docs/install/quick.html#linux-miniconda-install
- **Mac:** http://conda.pydata.org/docs/install/quick.html#os-x-miniconda-install
- **Windows:** http://conda.pydata.org/docs/install/quick.html#windows-miniconda-install

**Sign Up** on [Github](www.github.com) if you have not already done so.

**Install** [Github Desktop](https://desktop.github.com/) if you don't already have it.

---

## Environment Setup

Now it's time to download the repository for `DeepLearning-Workbooks`.

You can use the Github website or PowerShell/terminal for this, but the easiest way is to just use the Github website and Github Desktop.

**Fork** the repository with the Github Website:

- Go to the website for the repository [here](https://github.com/Mdcrab02/DeepLearning-Workbooks)
- In the upper right hand corner of the page click 'Fork'
- You should now be at a repository of the same name, but on your Github.
- Go ahead and click 'Clone or download' here, and follow the Github Desktop prompt and clone the repository into the default location.

**Open**  PowerShell/terminal, and type in the following:
```
cd C:\Users\Your_User_Name\Documents\GitHub\DeepLearning-Workbooks

conda env create -f environment.yml
```
You should now be watching a lot of stuff happening at the command line as Anaconda gathers package information and installs them into your newly created environment.  The environment will be called 'DeepLearning-Workbooks'.

**Enter** the following into PowerShell/terminal to verify your new environment is set up:
```sh
conda info --envs
```
You should see 'DeepLearning-Workbooks' in the list returned.

**Activate** the environment by entering the following into PowerShell/terminal:
```
activate DeepLearning-Workbooks
```

*Note*: If 'activate DeepLearning-Workbooks' returned and error, try 'source activate DeepLearning-Workbooks'.

Now you're ready to start working in Jupyter.  **Enter** the following into PowerShell/terminal:
```
jupyter notebook
```

Now a browser window for Jupyter notebook should pop up in your default browser.  You should see a bunch of files and folders from your repository including the 'Workbooks' folder with all of the notebooks.

**Navigate** to any one of the notebook files, and **Double Click** to open it.

---

### Uninstalling

To uninstall the environment:

```sh
conda env remove -n DeepLearning-Workbooks
```

---

### Notes

I mainly use Windows, so these instructions are more geared towards Windows users.
