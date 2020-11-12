# Clingo in Jupyter Notebook

This repository is a collection of interactive Jupyter Notebooks, where you can run answer set programs using clingo in a browser. 
We use [mybinder](https://mybinder.org/) for building and sharing the interactive environment for this repository. 
More information on how a Binder repository is built can be found [here](https://mybinder.readthedocs.io/en/latest/introduction.html).

## Usage

- First click on this binder badge to open a notebook server. [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/krr-up/notebook.git/main)
- Check out `sample.ipynb` for a small introduction on how to use clingo in Jupyter Notebooks.
- Use `%%clingo` : the magic cell command for running answer set program specificied in a cell.
- Use `!clingo` as a shell command for running an answer set program saved in a file.
- You can create a new notebook or upload an existing one in the Home Page or the specific folder of your instance of Jupyter notebook server. 
  After finishing the work, you can save the notebook on your device by downloading it.  
- Visit the branch `exercises` to access the notebooks relevant for the ASP course.
- The branch `examples` contains some notebooks with answer set programs, along with clingo and other [potasso systems](https://github.com/potassco/).
- To try other notebook user interfaces, check [this](https://mybinder.readthedocs.io/en/latest/howto/user_interface.html).

### Adding new notebooks

To add new notebooks, push them to the respective branch and launch with mybinder.
The launch process after every commit takes a while, as it rebuilds the Docker image. 
If the Binder repository has already been built once, then subsequent clicks on the Binder link will not re-trigger the build process and the launches will be quicker.

### Update the environment
  
To change the underlying environment, modify the configuration files in the binder folder.
After every commit, a docker image is built as per the configuration specified in the binder folder.
For a list of all configuration files available, check [this](https://mybinder.readthedocs.io/en/latest/using/config_files.html#config-files).
The configuration files used in this repository are:
1. **environment.yml** to install conda packages.
2. **postBuild** is a script that contains commands to be run after the whole repository has been built. 
  The one in this repository contains an example of creating an alias for a magic command that will be available to any notebook created after launch.         Similarly you can add more magic commands or other ipython codes that will be executed before starting the notebook server, and can be used by all the notebooks   in the repository.


