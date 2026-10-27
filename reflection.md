# Lab 5: Static Code Analysis — Reflection

## 1. What is static code analysis, and why is it useful?

Static code analysis examines source code without executing it. It helps identify potential bugs, security vulnerabilities, coding-style violations, and maintainability problems early in development.

## 2. What are the differences between Pylint, Bandit, and Flake8?

Pylint checks code quality, naming conventions, documentation, and potential programming issues. Bandit identifies common security weaknesses in Python code. Flake8 checks code style and formatting, including PEP 8 violations.

## 3. What issues did you identify and fix in this lab?

I improved function and variable naming, added docstrings, corrected formatting violations, replaced MD5 with SHA-256 for review ID generation, removed the hardcoded password, and handled invalid movie titles and empty movie collections. I also addressed the remaining static-analysis findings to improve the Pylint score and reduce Bandit warnings.

## 4. How did static analysis improve the quality of the program?

Static analysis provided systematic feedback about code quality, security, and formatting. Fixing the reported issues made the program more readable, maintainable, and robust. Running the tools again after the changes helped verify the improvements.
