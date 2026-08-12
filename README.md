# Sales Pipeline Forecasting
A sample project where we use ["CRM Sales Opportunities" dataset](https://mavenanalytics.io/data-playground/crm-sales-opportunities?utm_id=97757_v0_s00_e0_tv0&fbclid=IwY2xjawTokM1wZG9mA2V4dG4DYWVtAjExAHNydGMGYXBwX2lkATAAAR4VphoBSLuR5q-mRjrXRQzzz38XXXPatWQTWd38uTB9bilCJQFH7tPFXgcuYw_aem_Upz5vJtbajc-ZxeHkTvDBA) from Maven Analytics to experiment with Sales Forecasting Models

## Project initialization
#### Pre-requisites - you should only ever have to do this 1 time on your local computer
- Install [Github Desktop](https://desktop.github.com/download/)
- Install an IDE (Interactive Development Environment) like [PyCharm](https://www.jetbrains.com/pycharm/download/?section=mac)
- Install [Python 3.14 via brew](https://formulae.brew.sh/formula/python@3.14) and install [virtualenv](https://virtualenv.pypa.io/en/latest/)
```commandline
# Install Python 3.14 via brew
# After running brew install, you should get the path of the python executable. It might look like '/opt/homebrew/bin/python3.14'. Save this path.
brew install python@3.14

# Install virtualenv
pip install virtualenv
```
#### Project setup - you should only have to do this the first time you set up a project
1. One person on the team creates the project repository and adds other Github contributors under project Settings > Collaborators
2. Each person on the team opens the project on their local computer, using Github Desktop
3. Each person sets up a virtual environment, using `virtualenv` and the same python version as everyone else (see steps below)
4. Each person opens up the project in Pycharm and links up the project to the virtual environment: PyCharm > Settings > Python > Interpreter > Add Interpreter > Add Local Interpreter > Select Existing > Select the path to the virtual environment python. Example: /Users/gyoo/projects/sales-pipeline-forecasting/venv/bin/python 
5. Each person creates a folder called 'data' and adds the downloaded .csv files to it

#### Setting up a virtual environment for the first time, using Python 3.14
The easy way... Python 3.14 already has the alias 'python3'. So if you use 'python3', you get Python 3.14.
```commandline
# use which to get the version of an executable (like python3)
which python3

# you should get a path to a python executable, it might look something like '/opt/homebrew/bin/python3.14'
# copy this entire path into terminal
/opt/homebrew/bin/python3.14

# if this is Python3.14, it will look like this:
# Python 3.14.6 (main, Jun 10 2026, 10:03:53) [Clang 17.0.0 (clang-1700.6.4.2)] on darwin
# Type "help", "copyright", "credits" or "license" for more information.

# make sure you are IN the project root
cd sales-pipeline-forecasting

# create the virtual environment, name it "venv", using 
virtualenv venv --python  $(which python3)
```

Easy way doesn't work? That's probably because the alias 'python3' is referring to a different version. Find out the exact path of the Python 3.14 executable and pass that to the `--python` flag
```commandline
# Get the path of the python executable through any means possible. It might look like '/opt/homebrew/bin/python3.14'. Save this path.

# make sure you are IN the project root
cd sales-pipeline-forecasting

# create the virtual environment, name it "venv", using Python 3.14
# instead of /opt/homebrew/bin/python3.14, you will put YOUR path to the python 3.14 executable
virtualenv venv --python  /opt/homebrew/bin/python3.14
```

#### Daily project use
Install a Python package into your virtual environment, so that you can access it in Pycharm
```commandline
# make sure you are IN the project root
cd sales-pipeline-forecasting

# activate the virtual environment
source venv/bin/activate

# install something, like the 'pandas' package
pip install pandas

# when you're done working on the project for the day, deactivate the virtual environment
deactivate
```


