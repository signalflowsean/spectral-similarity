# Spectral Similarity - Backend

## Getting Started
Follow these instructions to get an instance of the server and db up and running locally. 
**Disclaimer**: Only Mac OS was tested...  

### Install Requirements
#### Install python2
`brew install python@2`

#### Change default version of python in zhrc
**Open .zshrc file:** `open ~/.zshrc`

**Edit python alias or make a new one:** `alias python=/usr/local/bin/python2.7`

#### Udate PIP
`python -m pip install --upgrade pip`

**NOTE:** The `python -m pip install [...]` command installs python packages using the current version of python and not pip 


#### Install MySQL

`brew install mysql`

### Virtual Env

#### Install VirtualEnv

```
cd backend
python -m pip install virtualenv
```

#### Create Virtual Environment
`python -m virtualenv -p python env --always-copy`

#### Activate Virtual Environment

`source env/bin/activate`

### Install Dependencies

`env/bin/pip install -r requirements.txt`


`python -m pip install -r requirements.txt`

#### Save Dependencies
**THIS STEP IS FOR DEVS ONLY** 

**Install pipreqs**
 
`python -m pip install pipreqs`

**Save Dependencies**

`pipreqs --force "$(pwd)"`

### Conntect to DB
#### Check if MySQL is installed
`msyql -uroot -p`

#### Initialize Flask DB
`flask db init`

#### Create DB Migration
`flask db migrate`

#### Apply DB Migration
`flask db upgrade`

### AWS
#### Install AWS CLI
`brew install awscli`

#### Configure AWS
`... tbd`

### And Finally ...
#### Start Project 
```
export FLASK_CONFIG=development
export FLASK_DEBUG=1
export FLASK_APP=run.py
flask run
```

### Useful Commands
**List all of the currently installed python packages**

`pip freeze`

**Uninstall all pip packages**

` pip freeze | xargs pip uninstall -y`


**Installing MySQL-Python**
`sudo pip install MySQL-Python --global-option=build_ext --global-option="-I/usr/local/opt/openssl/include" --global-option="-L/usr/local/opt/openssl/lib"`
`
## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```
### References

Routes and db calls for project
#### [Flask Documentation](https://buildmedia.readthedocs.org/media/pdf/flask/rtd/flask.pdf)
