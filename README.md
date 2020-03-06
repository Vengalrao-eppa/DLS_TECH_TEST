Software Engineer Python Test

Create a REST endpoint that return the sum of a list of numbers e.g. [1,2,3] => 1+2+3 = 6 You are free to use any Python 3 framework, however, try and keep the usage of the third- party library to a minimum.

The list of numbers is expected to arrive from a backend service and for this test you can hard code the list using the following line.
numbers_to_add = list(range(10000001))

The url of the endpoint and the sample response is as follows: Request: http://localhost:5000/total
Response:
{
"total": 6
}
Please provide the source code, tests, documentations and any assumptions you have made.
Note: We are looking for the candidate’s “Software Engineering” ability not just the Python programming skills.


INSTALLATION:

- Python3 installation instructions: https://realpython.com/installing-python/
- Create a project directory dedicated for this application.
- Place 'rest_endpoint.py' and 'unit_tests.py' inside the project directory.

From inside the project directory:

- Enable virtual environment:

$ python3 -m venv env

- Activate the virtual environment:

source env/bin/activate

- Flask installation: 

$ pip install Flask


TESTING:
(unit_tests.py)

The 6 unit tests check the bahaviour of the application with 6 different list types: 
 - current list hardcoded in the application;
 - an empty list;
 - list which is bigger than the maximum allowed size;
 - list with mixed type elements;
 - list with negative numbers;
 - list with mixed number types, including integers and floats.


- While virtual environment is still active, run the unit test first, from the project directory:

$ python3 unit_tests.py

All 6 tests should pass

RUNNING:
(resst_endpoint.py)

- While virtual environment is still active, run 'rest_endpoint.py' from within the project directory:

$ python3 rest_endpoint.py

- On a web-browser, navigate to: http://localhost:5000/total

- After running the application, you can deactivate the virtual environment by running: 
 
$ deactivate


ASSUMPTIONS:

- Application is run in an environment which supports Python3 and third-party libraries used
- Application is run in an environment which allows HTTP requests to localhost and does not have any process occupying port 5000
- This application will not have widespread use therefore testing is done only on code’s critical behaviours