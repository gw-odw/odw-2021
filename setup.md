# Software Setup

In order to be able to execute the notebooks with the tutorials, you should configure your workspace following one of the options below.

They are listed in order of difficulty. However, we encourage the participants with some experience with Python environments to follow **Option3**, installing the requirements on their laptops and executing the tutorial notebooks from there. This has the advantage of avoiding any possible issue with online servers, including unstable internet connection or uneven memory and server availability, both on Colab and on MyBinder.

## Option 1: Google Colab

<img src='https://www.wispresort.com/uploadedImages/Winter/easy.png' width=20 /> Easy (No software installation; Works for any OS)

<img src='./share/video-icon.png' width=18 /> [Video instructions](https://drive.google.com/file/d/17jYkGoVIavJa1B_Fbi6xK2D3jCFQT-A7/view?usp=sharing)

1. Visit https://colab.research.google.com

2. Click the GITHUB tab

3. Enter "gw-odw/odw-2021" in the search bar, and click enter to search

4. Double click the notebook of your choice

5. At the top of the notebook, uncomment any `pip install` commands by removing the `#`

    `#! pip install -q 'gwosc==0.5.4`  <-- Remove the `#` and run

    (a pop-up warning message will probably show up:
    
    `WARNING: This notebook was not authored by Google.`
    
    Don't worry it is an expected behaviour)

6. Click `run all` from the `runtime` menu at the top

<div class="alert alert-info">If you are not familiar with google Colab, you can beforehand take a look at the guides offered by Google at  <a href="https://colab.research.google.com/notebooks/">this link</a>, in the "Examples" tab. In particular, it is recommended to have a certain understanding of the main features of notebooks, which you can learn in <a href="https://colab.research.google.com/notebooks/basic_features_overview.ipynb">this tutorial</a>.</div>

## Option 2: Run in mybinder

<img src='https://www.wispresort.com/uploadedImages/Winter/easy.png' width=20 /> Easy (No software installation; Works for any OS)

<img src='./share/video-icon.png' width=18 /> [Video instructions](https://drive.google.com/file/d/1QkjdG6IHeTWq2XtPreakLydaZMedJCrX/view?usp=sharing)

Just click the button below

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/gw-odw/odw-2021/master)

or visit [mybinder.org](https://mybinder.org/), paste in the "GitHub repository name or URL" cell the following address `https://github.com/gw-odw/odw-2021/`, and hit the `Launch` button. 

This will build a Docker image (if not already present) with the dependency file `environment.yml`. Then a [JupyterHub](https://jupyterhub.readthedocs.io/en/latest/) server will be open hosting the contents of the `gw-odw/odw-2021` repo. Check the Jupyter notebooks with the tutorials for the various days in the corresponding folders. 

## Option 3: You have a Linux or Apple/Mac computer -- Use conda

<img src='https://www.wispresort.com/uploadedImages/Winter/intermediate.png' width=20 /> Intermediate (Some software installation; Will not work on Windows PC)

<img src='./share/video-icon.png' width=18 /> [Video instructions](https://drive.google.com/file/d/1YZcaY-35JiHXOH4unRe5ECSeDl8IZFZy/view?usp=sharing)

**Note:** this workshop will use Python version 3.8

1. Install miniconda:
   
    - Visit the website https://conda.io/en/latest/miniconda.html
    - Choose the version for Python 3.8
    - See the installation instructions here: https://conda.io/projects/conda/en/latest/user-guide/install/

        - [Linux](https://docs.conda.io/projects/conda/en/latest/user-guide/install/linux.html)
        - [macOS](https://docs.conda.io/projects/conda/en/latest/user-guide/install/macos.html)
    
   You may need to restart your computer after installation.

2. Download the IGWN YML file for the [IGWN Conda Distribution](https://computing.docs.ligo.org/conda/environments/igwn-py38/)
   * [YML file for linux](./environment.yml)
   * [YML file for macOS](./igwn-py38-macOS.yaml)

   **Note:** the `igwn-py38` dependencies files saved in this repository have been both tested working. If you prefer having the most recent release of the same environment dependencies, you can visit the [IGWN website](https://computing.docs.ligo.org/conda/) and download the one corresponding to your OS directly from there.

3. Add the conda-forge channel <br/>
    `conda config --add channels conda-forge`

4. Create the environment: <br/>
   * On Linux: `conda env create --file environment.yml`
   * On macOS: `conda env create --file igwn-py38-macOS.yaml`

5. Clone the workshop git repo <br/>
    `git clone https://github.com/gw-odw/odw-2021.git`

6. Move into the directory with the workshop git repo <br/>
    `cd odw-2021`
    
7. Activate the environment <br/>
  `conda activate igwn-py38`

8. Build a custom [jupyter kernel](https://ipython.readthedocs.io/en/stable/install/kernel_install.html) using the command <br/>
  `ipython kernel install --user --name=igwn-py38` <br/>
  or equivalently <br/>
  `python -m ipykernel install --user --name=igwn-py38`

9. Start the Jupyter notebook server <br/>
  `jupyter notebook` and select the kernel `igwn-py38` if this is not done by default.

**Notebooks:**
If you are not familiar with Jupyter notebooks, google one of the many introductory guides available on the internat, like <a href="https://realpython.com/jupyter-notebook-introduction/">this one</a>. Also, taking a look at the <a href="https://colab.research.google.com/notebooks/basic_features_overview.ipynb">Examples</a> offered by Google Colab can be helpful.

**Troubleshooting:**
- The kernel `igwn-py38` should appear in the list returned by the command `jupyter kernelspec list` executed in a terminal
- If, when you run jupyter, you get the message: `Could not find kernel matching igwn-py38. Please select a kernel: Python 3`
this indicates the `igwn-py38` kernel is not installed properly. Make sure you executed step 9)

## Option 4: Linux install on Windows 10 with dedicated app (Windows 10 only)

<img src='https://www.wispresort.com/uploadedImages/Winter/hard.png' width=20 /> Advanced (For Windows 10)

Install a Linux distribution on your Windows system. 
See instructions here: https://docs.microsoft.com/en-us/windows/wsl/install-win10

We suggest you install Debian GNU/Linux, which is the closest distribution to what is 
used currently by LIGO/Virgo. Once you have Linux installed, follow the instructions 
in Option 3.

