# NLPCapstone
**Udacity - Artificial Intelligence Nanodegree Program**   
AI - Natural Language Processing Project

# Natural Language Processing

![GANImage](/images/bidirectional.png)

This project is part of **Udacity´s Artificial Intelligence Nanodegree Program**. Here you will find my personal solution to the challenge. The following project can be run using a Local Machine or using an external GPU (Solution provided by **Amazon Web Services** is recommended). Next, you can follow Udacitys instructions to install the necessary dependencies on a local machine or on AWS.


Follow the instructions to install the required environment and check the jupyter notebook file:

    (pmaienv)$ jupyter notebook machine_translation.ipynb
  
--------------------------------------------------------------------------------------------------------

### Instructions - Udacity Project

## Project Requirements
# Introduction
In this notebook, you will build a deep neural network that functions as part of an end-to-end machine translation pipeline. Your completed pipeline will accept English text as input and return the French translation.

# Setup

This project requires GPU acceleration to run efficiently. Support is available to use either of the following two methods for accessing GPU-enabled cloud computing resources.

## Udacity Workspaces (Recommended)

Udacity Workspaces provide remote connection to GPU-enabled instances right from the classroom. Refer to the classroom lesson for this project to find an overview of navigating & using Jupyter notebook Workspaces.

## Amazon Web Services (Optional)

Please refer to the Udacity instructions for setting up a GPU instance for this project, and refer to the project instructions in the classroom for setup. The recommended AMI should include compatible versions of all required software and libraries to complete the project. [link for AIND students](https://classroom.udacity.com/nanodegrees/nd889/parts/16cf5df5-73f0-4afa-93a9-de5974257236/modules/53b2a19e-4e29-4ae7-aaf2-33d195dbdeba/lessons/2df3b94c-4f09-476a-8397-e8841b147f84/project)

## Install
- Python 3
- NumPy
- TensorFlow 1.x
- Keras 2.x

# Submission
When you are ready to submit your project, do the following steps:
1. Ensure you pass all points on the [rubric](https://review.udacity.com/#!/rubrics/1004/view).
2. Submit the following in a zip file:
  - `helper.py`
  - `machine_translation.ipynb`
  - `machine_translation.html`

## Converting to HTML

There are several ways to generate an HTML copy of the notebook:

 - Running the last cell of the notebook will export an HTML copy

 - Navigating to **File -> Download as -> HTML (.html)** within the notebook

 - Using `nbconvert` from the command line

    $ pip install nbconvert
    $ nbconvert machine_translation.ipynb
     
--------------------------------------------------------------------
--------------------------------------------------------------------

### Instructions 2

1. (Optional) __If you plan to install TensorFlow with GPU support on your local machine__, follow [the guide](https://www.tensorflow.org/install/) to install the necessary NVIDIA software on your system.  If you are using an EC2 GPU instance, you can skip this step.

2. (Optional) **If you are running the project on your local machine (and not using AWS)**, create (and activate) a new environment.

	- __Linux__ (to install with __GPU support__, change `requirements/pmaienv-linux.yml` to `requirements/pmaienv-linux-gpu.yml`): 
	```
	  $ conda env create -f requirements/pmaienv-linux.yml
    $ source activate pmaienv-project
	```  
	- __Mac__ (to install with __GPU support__, change `requirements/pmaienv-mac.yml` to `requirements/pmaienv-mac-gpu.yml`): 
	```
    $ conda env create -f requirements/pmaienv-mac.yml
    $ source activate pmaienv-project
	```  
	- __Windows__ (to install with __GPU support__, change `requirements/pmaienv-windows.yml` to `requirements/pmaienv-windows-gpu.yml`):  
	```
    $ conda env create -f requirements/pmaienv-windows.yml
    $ activate pmaienv-project
	```
	
3. (Optional) **If you are running the project on your local machine (and not using AWS)** and Step 6 throws errors, try this __alternative__ step to create your environment.

	- __Linux__ or __Mac__ (to install with __GPU support__, change `requirements/requirements.txt` to `requirements/requirements-gpu.txt`): 
	```
    $ conda create --name pmaienv-project python=3.5
    $ source activate pmaienv-project
    (pmaienv)$ pip install -r requirements/requirements.txt
	```  
	- __Windows__ (to install with __GPU support__, change `requirements/requirements.txt` to `requirements/requirements-gpu.txt`):  
	```
    $ conda create --name pmaienv-project python=3.5
    $ activate pmaienv-project
    (pmaienv)$ pip install -r requirements/requirements.txt
	```
	
4. (Optional) **If you are using AWS**, install Tensorflow.
```
    (pmaienv)$ sudo python3 -m pip install -r requirements/requirements-gpu.txt
```
	
5. Switch [Keras backend](https://keras.io/backend/) to TensorFlow.
- __Linux__ or __Mac__: 
```
    (pmaienv)$ KERAS_BACKEND=tensorflow python -c "from keras import backend"
```
- __Windows__: 
```
    (pmaienv)$ set KERAS_BACKEND=tensorflow
     python -c "from keras import backend"
```

6. (Optional) **If you are running the project on your local machine (and not using AWS)**, create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `pmaienv-project` environment. 
```
    (pmaienv)$ python -m ipykernel install --user --name pmaienv-project --display-name "pmaienv-project"
```

7. Launch Jupyter notebook.
```
    (pmaienv)$ jupyter notebook machine_translation.ipynb
```

8. (Optional) **If you are running the project on your local machine (and not using AWS)**, before running code, change the kernel to match the pmaienv-project environment by using the drop-down menu (**Kernel > Change kernel > pmaienv-project**). 
