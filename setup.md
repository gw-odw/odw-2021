# Software Setup

Choose an option below.

## Option 1: Google co-labs

<img src='https://www.wispresort.com/uploadedImages/Winter/easy.png' width=20 /> Easy (No software installation; Works for any OS)

[Video Guide](https://labcit.ligo.caltech.edu/~jkanner/gwosc/colab-help-2020.mov)

1. Visit https://colab.research.google.com

2. Click the GITHUB tab

3. Enter "gw-odw/odw-2021" in the search bar, and click enter to search

4. Double click the notebook of your choice

5. At the top of the notebook, uncomment any `pip install` commands by removing the `#`

  `#! pip install -q 'gwosc==0.5.4`  <-- Remove the `#` and run
    (a pop-up warning message will probably show up: `WARNING: This notebook was not authored by Google.` `Unrecognised runtime "igwin-py37"; defaulting to "python3"`. Don't worry it is an expected behaviour)

6. Click `run all` from the `runtime` menu at the top

## Option 2: Run in mybinder

<img src='https://www.wispresort.com/uploadedImages/Winter/easy.png' width=20 /> Easy (No software installation; Works for any OS)

Just click the button below

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/gw-odw/odw-2021/master)

or visit [mybinder.org](https://mybinder.org/), paste in the "GitHub repository name or URL" cell the following address `https://github.com/gw-odw/odw-2021/`, and hit the `Launch` button. 

This will build a Docker image (if not already present) with the dependency file `environment.yml`. Then a [JupyterHub](https://jupyterhub.readthedocs.io/en/latest/) server will be open hosting the contents of the `gw-odw/odw-2021` repo. Check the Jupyter notebooks with the tutorials for the various days in the corresponding folders. 

## Option 3: You have a Linux or Apple/Mac computer -- Use conda

<img src='https://www.wispresort.com/uploadedImages/Winter/intermediate.png' width=20 /> Intermediate (Some software installation; Will not work on Windows PC)

Note: this workshop will use Python version 3.7

1. Install miniconda: https://conda.io/en/latest/miniconda.html <br/>

    Choose the version for Python 3.7. 
    
    See the installation instructions here: https://conda.io/projects/conda/en/latest/user-guide/install/
    
    You may need to restart your computer after installation.

2. Download the IGWN YML file for the [IGWN Conda Distribution](https://computing.docs.ligo.org/conda/environments/igwn-py37/)
   * [YML file for linux](./environment.yml)
   * [YML file for osx  ](./igwn-py37-osx.yaml)

3. Add the conda-forge channel <br/>
    `conda config --add channels conda-forge`

4. Create the environment <br/>
    `conda env create --file igwn-py37.yaml`

5. Clone the workshop git repo <br/>
    `git clone https://github.com/gw-odw/odw-2021.git`

6. Move into the directory with the workshop git repo <br/>
    `cd odw-2021`
    
7. Activate the environment <br/>
  `conda activate igwn-py37`

8. Build a custom jupyter kernel using the command <br/>
  `ipython kernel install --user --name=igwn-py37` <br/>
  or equivalently <br/>
  `python -m ipykernel install --user --name=igwn-py37`

9. Start the jupyter notebook server <br/>
  `jupyter notebook` and select the kernel `igwn-py37` if this is not done by default.

Troubleshooting:
- The kernel `igwn-py37` should appear in the list returned by the command `jupyter kernelspec list` executed in a terminal
- If, when you run jupyter, you get the message: `Could not find kernel matching igwn-py37. Please select a kernel: Python 3`
this indicates the `igwn-py37` kernel is not installed properly. Make sure you executed step 9)

## Option 4: Linux install on Windows 10 with dedicated app (Windows 10 only)

<img src='https://www.wispresort.com/uploadedImages/Winter/hard.png' width=20 /> Advanced (For Windows 10)

Install a Linux distribution on your Windows system. 
See instructions here: https://docs.microsoft.com/en-us/windows/wsl/install-win10

We suggest you install Debian GNU/Linux, which is the closest distribution to what is 
used currently by LIGO/Virgo. Once you have Linux installed, follow the instructions 
in Option 3.

