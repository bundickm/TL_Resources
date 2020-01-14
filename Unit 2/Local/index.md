[DS](/ds) > [Unit 2](/ds/unit2) > Local Setup


# Local Setup

1. Install Anaconda
2. Open your operating system's command line
3. Set up Git for command line
4. Create conda environment
5. Install packages
6. Launch Jupyter Notebook

# 1. Install Anaconda


[Download the Anaconda installer](https://www.anaconda.com/distribution/), Python 3.7 version, for your operating system: Windows, macOS, or Linux.

Then run the Installer you downloaded. ([Anaconda has more documentation available.](https://docs.anaconda.com/anaconda/install/))

# 2. Open your operating system's command line

**Windows** users, [open **Anaconda Prompt**.](https://docs.anaconda.com/anaconda/user-guide/getting-started/#open-anaconda-prompt) (Not Powershell, Cmd, or Git Bash.)

**Mac** users, [open **Terminal**.](https://support.apple.com/guide/terminal/open-or-quit-terminal-apd5265185d-f365-44cb-8b09-71a064a42125/mac)

This 1 minute video explains why we want to help you get comfortable with the command line:

<iframe width="560" height="315" src="https://www.youtube.com/embed/P3j2uu9tcyk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# 3. Set up Git for command line

<iframe width="560" height="315" src="https://www.youtube.com/embed/aoDte_AOUXs" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

**Windows** users, [download and install Git for Windows](https://gitforwindows.org/).

**Mac** users, you don't need to download Git, it is built in for you.

All users, use your command line to [set up Git](https://help.github.com/en/github/getting-started-with-github/set-up-git). First, enter this command, to [set your username in Git](https://help.github.com/en/github/using-git/setting-your-username-in-git):

```
git config --global user.name "Mona Lisa"
```

Then, [set your commit email address](https://help.github.com/en/github/setting-up-and-managing-your-github-user-account/setting-your-commit-email-address):

```
git config --global user.email "email@example.com"
```

# 4. Create conda environment

A [conda environment](https://docs.anaconda.com/anaconda/navigator/glossary/#navigator-glossary-conda-environment) "contains a specific collection of conda packages and their dependencies, so they can be maintained and run independently without interfering with each other." 

We use conda environments to help our projects be reproducible and prevent [conflicts](https://www.explainxkcd.com/wiki/index.php/1987:_Python_Environment) between projects. (Want to learn more? We recommend [The Definitive Guide to Conda Environments](https://towardsdatascience.com/a-guide-to-conda-environments-bc6180fc533).)


Enter this command, to [create a conda environment](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-with-commands) named `unit2`, with Python 3.7.

```
conda create -n unit2 python=3.7
```

# 5. Install packages

A [conda package](https://docs.anaconda.com/anaconda/navigator/glossary/#navigator-glossary-conda-pkg) "contains everything that a software program needs in order to be installed and run, so you do not have to manually find and install each dependency separately. This can include system-level libraries, Python modules, executable programs and other components. Managed with conda or Anaconda Navigator." 

[Activate the environment:](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#activating-an-environment)

```
conda activate unit2
```

[Add the conda-forge channel.](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-channels.html) "Conda channels are the locations where packages are stored. They serve as the base for hosting and managing packages."

```
conda config --add channels conda-forge
```

[Install](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-pkgs.html#installing-packages) these packages used in Unit 2. (Anaconda will also automatically install any dependencies of these packages, including
matplotlib, numpy, pandas, python-graphviz, and scikit-learn.)

```
conda install category_encoders eli5 jupyter pandas-profiling pdpbox plotly py-xgboost seaborn shap
```

# 6. Launch Jupyter Notebook

```
conda activate unit2
```

```
jupyter notebook
```

Congratulations, you have launched a Jupyter Notebook in the unit2 conda environment!
