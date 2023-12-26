### Conceptual Exercise

Answer the following questions below:

- What are important differences between Python and JavaScript?
Python is often used as a server-side language (Django, Flask), for scientific computing, and scripting.
JavaScript is primarily used for client-side scripting in web browsers, but with the advent of Node.js, it can also be used on the server side.



- Given a dictionary like ``{"a": 1, "b": 2}``: , list two ways you
  can try to get a missing key (like "c") *without* your programming
  crashing.
1- Using the get Method:
my_dict = {"a": 1, "b": 2}
value = my_dict.get("c", None)

2- Using Exception Handling:
my_dict = {"a": 1, "b": 2}
try:
    value = my_dict["c"]
except KeyError:
    value = None






- What is a unit test?
A unit test is a type of software testing where individual units or components of a software application are tested in isolation. The purpose is to validate that each unit of the software performs as designed.



- What is an integration test?
An integration test is a type of software testing that tests the integration or interaction between different components or systems. The goal is to ensure that the integrated components work together as expected.



- What is the role of web application framework, like Flask?
A web application framework, like Flask, provides a structured way to build and organize web applications. It simplifies common tasks such as handling HTTP requests, managing routes, and connecting to databases. Flask follows the WSGI (Web Server Gateway Interface) standard, making it easy to integrate with different web servers.



- You can pass information to Flask either as a parameter in a route URL
  (like '/foods/pretzel') or using a URL query param (like
  'foods?type=pretzel'). How might you choose which one is a better fit
  for an application?



- How do you collect data from a URL placeholder parameter using Flask?
@app.route('/foods/<food_type>')
def get_food(food_type):
    # Access 'food_type' here




- How do you collect data from the query string using Flask?
from flask import request

@app.route('/foods')
def get_food():
    food_type = request.args.get('type')
    # Access 'food_type' here




- How do you collect data from the body of the request using Flask?
from flask import request

@app.route('/foods', methods=['POST'])
def create_food():
    food_type = request.form.get('type')
    # Access 'food_type' here




- What is a cookie and what kinds of things are they commonly used for?
A cookie is a small piece of data stored on the client's browser. It is commonly used for:
Session management (user authentication).
Personalization (remembering user preferences).
Tracking user behavior (analytics).



- What is the session object in Flask?
In Flask, the session object is a dictionary-like object that allows you to store data across requests. It uses cookies to store a session identifier on the client side and keeps the data on the server side.



- What does Flask's `jsonify()` do?
'jsonify()' is a method in Flask that converts a Python dictionary or other data types into a JSON response. It sets the appropriate content type and returns a JSON-formatted response that can be sent to the client.
