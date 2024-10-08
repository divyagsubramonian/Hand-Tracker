Before working with the code in this repo, you should:

# Getting started with OpenCV on Python

In this repo, we are working with this tutorial, and
trying to get it working on Mac.

* <https://www.section.io/engineering-education/creating-a-hand-tracking-module/>

# Setup steps

The version of Python that happens to be on our Mac may or may not
be compatible with opencv.

So, we first install a couple of tools to help:

# Installing homebrew

To install homebrew, visit <https://brew.sh> and copy the command from
there to install Homebrew.  It may take a while.

Afterwards, you might see an error message such as this one:

<img width="687" alt="image" src="https://github.com/ccs-1l-f23/opencv-python-spike/assets/1119017/83b14328-56b6-46fb-ba75-56fe84d9f401">

If you get that, then put in the command it suggests.  It may take a very long time before you see any output (5-10 minutes), so be patient.

Eventually, though, it should finish. After that, type `brew update`.  Then you are ready for the next step.

# Installing pyenv and it's dependencies

We got the idea to install pyenv because we were not able to use opencv with the default version of Python on our mac.

So we read this article: <https://medium.com/macoclock/how-to-install-and-manage-multiple-python-versions-on-macos-ca01a5e398d4>

To install pyenv, use these commands:

```
brew install pyenv
brew install openssl readline sqlite3 xz zlib
```

Then you are ready to create a virtual environment and set it up using a particular version of Python

# Setting up opencv

First, install this version of Python:

```
pyenv install  3.9.18   
```

# Install virtualenv

To install virtualenv, use:

```
pip install virtualenv
```

# Creating your virtualenv

For the next instructions, you should create a new empty git repo (or at the very least, create a new empty directory).

Then, create a `venv` ( a Python virtual environment) using that version of Python:

```
virtualenv venv --python=python3.9
```

Activate the virtual environment with this command.  (This is the only command that you might actually need to do every time you start a new
terminal session for this project.)

```
source venv/bin/activate
```

Then install your dependencies, and opencv:

```
pip install mediapipe
pip install opencv-python
```

