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

pip install flask-sqlalchemy

python
from flaskblog import db
db.create_all()

from flaskblog import User, Post
user_1 = User(username='Corey', email='C@demo.com', password='password')
db.session.add(user_2)

user_2 = User(username='JohnDoe', email='jd@demo.com', password='password')
db.session.add(user_2)

db.session.commit()

User.query.all()
User.query.first()
User.query.filter_by(username='Corey').all()
User.query.filter_by(username='Corey').first()

user = User.query.filter_by(username='Corey').first()
user
user.id
user = User.query.get(1)
user
user.posts

post_1 = Post(title='Blog 1', content='First Post Content!', user_id=user.id)
post_2 = Post(title='Blog 2', content='Second Post Content!', user_id=user.id)
db.session.add(post_1)
db.session.add(post_2)
db.session.commit()

user.posts

for post in user.posts:
    print(post.title)

post = Post.query.first()
post
post.user_id
post.author


db.drop_all()
db.create_all()
User.query.all()
Post.query.all()

# 05 Package Structure

python
from flaskblog import db
from flaskblog.models import User, Post  
db.create_all()
User.query.all()


# 06 User Authentication

pip install flask-bcrypt

python
from flask_bcrypt import Bcrypt
bcrypt = Bcrypt()
bcrypt.generate_password_hash('testing')
bcrypt.generate_password_hash('testing').decode('utf-8')
hashed_pw = bcrypt.generate_password_hash('testing').decode('utf-8')
bcrypt.check_password_hash(hashed_pw, 'password')
bcrypt.check_password_hash(hashed_pw, 'testing')


(2)
python
from flaskblog import db
from flaskblog.models import User
user = User.query.first()
user
user.password

(3)

pip install flask-login


# 07 User Account Profile Pic

pip install Pillow



# 08 Posts