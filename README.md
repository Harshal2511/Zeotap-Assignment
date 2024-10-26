# Zeotap-Assignment

#Assigment no 1: Rule Engine with AST
Step1: Create Backend with Python
  a: Set Up Flask for the Backend
  b: Create Flask API: Save the Python code in a file called app.py.
  c: Run the Flask Server: python app.py, This will start the server on http://127.0.0.1:5000.

Step 2: Create the Frontend with HTML and JavaScript
  Saved all the HTML code in a file called index.html.

Explanation of Frontend
 1. Create Rule Section:
    Input a rule string and click Create Rule.
    The rule is sent to the backend’s /create_rule endpoint to be parsed and stored.

 2. Combine Rules Section:
    Select an operator (AND or OR) and click Combine Rules.
    This sends a request to the backend’s /combine_rules endpoint to merge all created rules into one combined AST.
  
 3. Evaluate Rule Section:
    Enter a JSON object representing data attributes and click Evaluate.
    This sends the data to the /evaluate_rule endpoint, which evaluates it against the combined AST and returns the result (True or False).

* Running the Application:
  1. Run the Flask server with python app.py.
  2. Open index.html in a web browser.
  3. Interact with the UI by creating, combining, and evaluating rules.
