# Static Code Analysis Issues

| Issue | Type | Original Location | Description | Fix Approach |
|---|---|---|---|---|
| Unsafe `eval()` usage | Security | Line 42 | Evaluated an expression supplied as a string, which could execute unintended code. | Replaced expression evaluation with validated numeric discount input. |
| Hard-coded secret | Security | `main()` | A sensitive-looking token was stored directly in the source and printed. | Removed the hard-coded token and its output. |
| Mutable default argument | Code quality | Line 15 | A list used as a default argument could retain data between calls. | Changed the default to `None` and initialized a new list inside the function. |
| Bare exception handler | Code quality | Line 26 | A bare `except` could hide unexpected errors. | Removed the broad exception handler and handled missing seats explicitly. |
| Insecure hash choice | Security | Line 45 | MD5 is not suitable where collision resistance is required. | Replaced MD5 with SHA-256. |
| Missing docstrings | Code quality | Multiple lines | Functions lacked descriptions. | Added docstrings to explain function purposes. |
| Unspecified file encoding | Code quality | Line 55 | File operations did not explicitly define text encoding. | Specified UTF-8 encoding. |
| Unused imports and variables | Code quality | Multiple lines | Unused names made the code harder to maintain. | Removed unused imports and variables. |
| Naming and formatting violations | Style | Multiple lines | Function naming, string formatting and final-newline issues reduced consistency. | Used snake_case, f-strings and consistent formatting. |

*Note: The locations above refer to the original code. Confirm each location against the saved original reports.*
