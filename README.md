# Flask-Tutorials

# 01 Getting Started

https://github.com/CoreyMSchafer/code_snippets/tree/master/Python/Flask_Blog

(1)

pip list

python -m venv project_env

dir

project_env\Scripts\activate.bat
project_env\Scripts\activate.ps1

where python

(2)

pip install flask

python

import flask

mkdir Flask_Blog

(3)

cd Flask_Blog/

export FLASK_APP=flaskblog.py

$env:FLASK_DEBUG = 1

(4)

python flaskblog.py



# 02 Templates


# 03 Forms and User Input

(1)
pip install flask-wtf

(2)
python
import secrets
secrets.token_hex(16)

# 04 Database