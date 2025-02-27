# Lexical Analyzer in C

## Description
This program is a simple lexical analyzer for a subset of the C programming language. It takes a string of C-like code and identifies tokens, including keywords, operators, delimiters, integers, and identifiers. This tool could be useful for anyone looking to understand the basics of tokenization or creating a simple compiler for educational purposes.

## Features
The lexical analyzer can identify the following types of tokens:
1. **Keywords** - Standard C keywords (e.g., `int`, `float`, `while`, etc.).
2. **Operators** - Arithmetic and comparison operators (e.g., `+`, `-`, `*`, `/`, `=`, `<`, `>`, etc.).
3. **Delimiters** - Symbols that delimit expressions (e.g., spaces, commas, parentheses, etc.).
4. **Integers** - Whole numbers.
5. **Identifiers** - Variable names and other valid identifiers.
6. **Unidentified** - Tokens that do not fit into any recognized category.

## Usage
1. Clone or download the source code.
2. Compile the code with any C compiler. For example:
   ```bash
   gcc lexical_analyzer.c -o lexical_analyzer
   ```
3. Run the executable:
   ```bash
   ./lexical_analyzer
   ```

## Code Explanation

### Core Functions
- **`isDelimiter`**: Checks if a character is a delimiter.
- **`isOperator`**: Checks if a character is an operator.
- **`isValidIdentifier`**: Verifies if a string is a valid identifier.
- **`isKeyword`**: Checks if a string is a C keyword.
- **`isInteger`**: Checks if a string represents an integer.
- **`getSubstring`**: Extracts a substring from the given input based on start and end indices.
- **`lexicalAnalyzer`**: Parses the input code, identifies tokens, and prints their type and value.

### Example
In the example provided in `main`, the program analyzes the input string:
```c
int x=ab+bc+30+switch+ 0y
```
and outputs tokens it finds, labeling them as keywords, operators, identifiers, integers, or unidentified values.

### Sample Output
For the example input, you might see output similar to:
```
For Expression "int x=ab+bc+30+switch+ 0y ":
Token: Keyword, Value: int
Token: Identifier, Value: x
Token: Operator, Value: =
Token: Identifier, Value: ab
Token: Operator, Value: +
Token: Identifier, Value: bc
Token: Operator, Value: +
Token: Integer, Value: 30
Token: Operator, Value: +
Token: Keyword, Value: switch
Token: Operator, Value: +
Token: Unidentified, Value: 0y
```

## Customization
- **Add More Keywords**: Extend the `isKeyword` function to include more keywords if needed.
- **Enhance Valid Identifier Checking**: Modify `isValidIdentifier` to support more complex identifier rules.
  
## License
This project is open-source and available for modification and use in personal or educational projects.