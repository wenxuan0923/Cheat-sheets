### Web Development using Flask Python

1. Create new virtual environment
  > $ virtualenv <venv>

2. Activate virtual environment
  > $ venv\Scripts\activate.bat

3. Install flask in your vritual environment
  > $ pip install flask

4. Confirm that your virtual environment now has flask installed
  >  import flask

5. Create a package called app in your ve, that will host the application
  >  (venv) $ mkdir app

6. Create a __init__.py file inside app package

  >  from flask import Flask       # Creates the application object as an instance of class Flask      
  >  app = Flask(\_\_name\_\_)         # \_\_name\_\_ is a Python predefined variable      
  >  from app import routes        # this app refers to the folder/package app      

7. Create a routes.py file inside app package
The routes are the different URLs that the application implements.
In Flask, handlers for the application routes are written as Python functions, called view functions. 
View functions are mapped to one or more route URLs so that Flask knows what logic to execute when a client requests a given URL.

  >  from app import app      
  >  @app.route('/')               # A decorator modifies the function that follows it        
  >  @app.route('/index')        
  >  def index():        
  >      return "Hello, World!"        

8. To complete the application, you need to have a Python script at the top-level that defines the Flask application instance. 
Let's call this script microblog.py, and define it as a single line that imports the application instance:

  >  (venv) $ set FLASK_APP=microblog.py

9. Run your web application
  >  (venv) $ flask run

10. Type in url in your browser and review your app
  > - http://localhost:5000/index
  > - http://localhost:5000 
  > - http://localhost:5000/index 
