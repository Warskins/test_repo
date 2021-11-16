Productly is  a simple web application for managing departments and employees.

The web application  allow:
* display a list of departments and the average salary  for these departments
* display a list of employees in the departments with an indication of the salary for each employee 
* search for employees born on a certain date or in the period between dates
* change (add / edit / delete) the above data

<h3>Start application </h3>

1. Install python 3 and go to app folder.

2. Create virtual environment and install all necessary packages with pip.
```commandline
    python3 -m venv environment_name
    pip install -r requirements.txt
```

3. Open config.py and set up database URI.
   
4. Run create_db.py to create tables in database
```commandline
    python create_db.py
```

5. Use gunicorn to deploy application.
```commandline
    gunicorn main:app
```



<h3>Gests</h3>

1. Open bash in app directory

```comandline
    pytest # to run all tests
    pytest -s # to run and see all prints
    pytest tests/test_web.py # to run the test-script
```

2. Check test coverage

```comandline
    coverage run --omit='venv/*' -m pytest -v         
    coverage report
```
