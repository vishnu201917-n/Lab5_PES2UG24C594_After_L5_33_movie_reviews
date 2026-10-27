# Lab 5 — Static Code Analysis Issues

| Issue | Type | Line(s) | Description | Fix Approach |
|---|---|---:|---|---|
| Weak MD5 hashing | Security — High | 46 | Bandit B324 flags MD5 as a weak hashing algorithm. | Replace MD5 with SHA-256 for review ID generation. |
| Binding to all network interfaces | Security — Medium | 4 | Bandit B104 flags `0.0.0.0`, which allows a service to listen on all available network interfaces if used for binding. | Use `127.0.0.1` for local-only access in this demonstration. |
| Hardcoded password | Security — Low | 6 | Bandit B105 flags a password stored directly in source code. | Remove the unused password constant if it is not needed. |
| Standard random generator | Security — Low | 41 | Bandit B311 warns that `random` is not suitable for security-sensitive randomness. | Since featured movie selection is not security-sensitive, document the intended use or use a secure generator if required. |
| Missing module and function docstrings | Code quality | 1, 11, 16, 26, 34, 39, 45, 48, 54 | Pylint C0114 and C0116 report missing documentation. | Add a module docstring and concise docstrings to functions. |
| Non-standard function and argument names | Style | 11, 16, 26, 34, 39, 45, 48, 54 | Pylint C0103 flags camelCase names that do not follow Python naming conventions. | Rename functions and arguments using snake_case and update all calls. |
| Unnecessary else after return | Code quality | 28 | Pylint R1705 flags an unnecessary `else` after a return statement. | Remove the `else` and de-indent its body. |
| Unnecessary global statement | Code quality | 40 | Pylint W0603 flags the use of `global` in featured movie selection. | Refactor the function to return the selected movie and update the featured value in the caller, if appropriate. |
| Range and length iteration | Code quality | 50 | Pylint C0200 recommends `enumerate()` instead of iterating over `range(len(...))`. | Use `enumerate()` to access both index and title. |
| Missing whitespace around operator | Style | 35 | Flake8 E225 reports missing whitespace around an operator. | Add the required spaces around the assignment operator. |
| Missing blank lines before function | Style | 48 | Flake8 E302 expects two blank lines before a top-level function. | Add the required blank line. |
| Inline comment spacing | Style | 70 | Flake8 E261 requires at least two spaces before an inline comment. | Add the required spacing before the comment. |
| Missing whitespace after comma | Style | 72 | Flake8 E231 reports missing whitespace after a comma. | Add a space after the comma. |
