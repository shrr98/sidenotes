# Setup Virtualenv in PyCharm for Tensorflow Developer Certification

Requirements:
- Ubuntu 18.04
- PyCharm 2021.1.3

## Install Python 3.8
[NOTE] SKIP this section if you already have Python3.8 in your machine.
```bash
wget https://www.python.org/ftp/python/3.8.6/Python-3.8.6.tgz
tar -xzf Python-3.8.6.tgz
cd Python-3.8.6
./configure -enable-optimizations
make -j 4
sudo make install
```

## Install Virtualenv
[reference](https://naysan.ca/2019/08/05/install-python-3-virtualenv-on-ubuntu/)
```bash
# Step 1: Update your repositories
sudo apt-get update

# Step 2: Install pip for Python 3
sudo apt-get install build-essential libssl-dev libffi-dev python-dev
sudo apt install python3-pip

# Step 3: Use pip to install virtualenv
sudo pip3 install virtualenv 

# Step 4: Go to directory you want to keep your venv.
# and Launch your Python 3 virtual environment, here the name of my virtual environment will be env3
cd <directory>
virtualenv -p python3 env3

# Step 5: Activate your new Python 3 environment. There are two ways to do this
. env3/bin/activate # or source env3/bin/activate which does exactly the same thing

# you can make sure you are now working with Python 3
python -- version
# this command will show you what is going on: the python executable you are using is now located inside your virtualenv repository
which python 

# Step 6: code your stuff

# Step 7: done? leave the virtual environment
deactivate
```
## Install required libraries
1. Make sure you are in your virtualenv
  ```bash
  . env3/bin/activate
  ```
1. Save this to `requirements.txt`.
  ```
  tensorflow==2.5.0
  tensorflow-datasets==4.3.0
  Pillow==8.2.0
  pandas==1.2.4
  numpy==1.19.5
  scipy==1.7.0
  ```
3. Run this command to install the libraries:
  ```
  pip install -r requirements.txt
  ```
