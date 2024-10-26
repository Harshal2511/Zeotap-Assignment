# Zeotap-Assignment

#Assigment no 1: Rule Engine with AST
  This project is a web-based rule engine that uses an Abstract Syntax Tree (AST) to parse, combine, and evaluate rules based on user-defined criteria. The project includes a backend built with Flask and a simple frontend for user interaction, allowing you to create rules, combine them, and evaluate data against these rules in real-time.

 Features:
  *Define Rules: Users can input logical conditions to create rules.
  *Combine Rules: Combine multiple rules using logical operators (AND/OR).
  *Evaluate Rules: Evaluate combined rules based on user-provided data.
  *Interactive UI: Simple HTML/JavaScript interface to interact with the rule engine

  Usage:
    * Create Rule: Enter a rule in the format attribute operator value, using logical operators like AND and OR to combine conditions. 
      Example: age > 30 AND department == 'Sales'.
    * Combine Rules: After creating multiple rules, select an operator (AND/OR) and click "Combine Rules" to create a single rule tree.
    * Evaluate Rule: Input data as a JSON object to evaluate against the combined rules. Example: {"age": 35, "department": "Sales", 
      "salary": 60000}.

 API Endpoints
   The backend exposes the following endpoints:
   
   * POST /create_rule: Parses a rule string into an AST and stores it.
        Payload: { "rule_string": "<rule expression>" }
        Response: { "message": "Rule created", "ast": "<AST representation>" }

   * POST /combine_rules: Combines all created rules into a single AST using a specified operator.
         Payload: { "operator": "<AND or OR>" }
         Response: { "message": "Rules combined", "combined_ast": "<combined AST representation>" }

   * POST /evaluate_rule: Evaluates the combined rule against the provided data.
        Payload: { "data": { <attribute-value pairs> } }
        Response: { "result": true/false }
