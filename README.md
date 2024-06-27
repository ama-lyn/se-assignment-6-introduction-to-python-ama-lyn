[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/WfNmjXUk)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=15339157&assignment_repo_type=AssignmentRepo)
# SE-Assignment-6
 Assignment: Introduction to Python
Instructions:
Answer the following questions based on your understanding of Python programming. Provide detailed explanations and examples where appropriate.

 Questions:

## 1. Python Basics

_What is Python, and what are some of its key features that make it popular among developers? Provide examples of use cases where Python is particularly effective._

Python is an object oriented programming language. 

   Some of it's key features are:

      a. It is easy to learn because of it's syntax
      b. Has a lot of predefined modules 
      c. It is platform independent
      d. It is a high level language
      e. It is open source, has a larger community

   Some areas where python is used:

      a. Web development
      b. Data science
      c. Machine learning
      d. Game development


## 2. Installing Python

_Describe the steps to install Python on your operating system (Windows, macOS, or Linux). Include how to verify the installation and set up a virtual environment._

a. Go to the python official website 

b. Download the latest version of python

c. Install the downloaded file

d. Verify the installation by opening the command prompt and typing `python --version`

e. Set up a virtual environment by typing the following command in the command prompt `python -m venv <name of the virtual environment>`

f. Activate the virtual environment by typing the following command in the command prompt `source <name of the virtual environment>/Scripts/activate`


## 3. Python Syntax and Semantics

_Write a simple Python program that prints "Hello, World!" to the console. Explain the basic syntax elements used in the program._

```python
print ("Hello, World!")
```

print function is used to output text to the console, passes in the string "Hello, World!" as an argument. When run it outputs Hello World!


## 4. Data Types and Variables

_List and describe the basic data types in Python. Write a short script that demonstrates how to create and use variables of different data types._

Integers (int) - Whole numbers without fractional part

Float- Numbers with fractional part

Strings (str) - characters enclosed in single or double quotes

Booleans (bool) - Logical values, True or False

Lists (list) - Ordered collection of items which can be mixed data types

Tuple (tuple) - Ordered collection of similar items immutable

Dictionary (dict) - Unordered collection of key-value pairs

_Example of usage_

```python
#Integer
age = 30
print("Age:", age)

#String
name = "Alice"
print("Name:", name)

#Boolean
is_student = True
print("Is Student:", is_student)

#List
fruits = ["apple", "banana", "cherry"]
print("Fruits:", fruits)
```


## 5. Control Structures

_Explain the use of conditional statements and loops in Python. Provide examples of an `if-else` statement and a `for` loop._

Conditional statements are used to execute different blocks of code based on certain conditions.

`if-else` Statement
```python
age = 18

if age >= 18:
    print("You are an adult.")
else:
    print("You are a minor.")
```

`for` loop
```python
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print(fruit)
```

## 6. Functions in Python

_What are functions in Python, and why are they useful? Write a Python function that takes two arguments and returns their sum. Include an example of how to call this function._

Functions are blocks of reusable code that perform a specific task. Functions can take inputs, called arguments, and can return a value as output.

Some of the benefits are:

(a) Break down complex problems into smaller, manageable pieces.

(b) Write code once and reuse it multiple times without rewriting it.

(c) Make code easier to understand by grouping related operations together.

(d) Simplify updates and bug fixes by isolating functionality

_Example of function_

```python
def sum (a,b):
   return a+b

result = sum (19, 8) _Calling the function_
```

## 7. Lists and Dictionaries

_Describe the differences between lists and dictionaries in Python. Write a script that creates a list of numbers and a dictionary with some key-value pairs, then demonstrates basic operations on both._

A list is an ordered collection of elements, which can be of any type, and is indexed starting from 0. Lists are mutable.They are ideal for storing collections of items where order matters. 

A dictionary is an unordered collection of key-value pairs, where each key is unique and used to access its corresponding value. Dictionaries are also mutable and are optimized for retrieving values when the key is known.

```python

# Creating a list of numbers
numbers = [1, 2, 3, 4, 5]

# Creating a dictionary with key-value pairs
student_grades = {
    "Alice": 90,
    "Bob": 85,
    "Charlie": 92
}

# Basic Operations on List

# Accessing elements
print("First number in list:", numbers[0])  # Output: 1

# Modifying elements
numbers[1] = 20
print("Modified list:", numbers)  # Output: [1, 20, 3, 4, 5]

# Adding elements
numbers.append(6)
print("List after adding an element:", numbers)  # Output: [1, 20, 3, 4, 5, 6]

# Removing elements
numbers.remove(3)
print("List after removing an element:", numbers)  # Output: [1, 20, 4, 5, 6]

# Basic Operations on Dictionary

# Accessing values by keys
print("Name:", person["name"])  # Output: Alice

# Modifying values
person["age"] = 31
print("Modified dictionary:", person)  # Output: {'name': 'Alice', 'age': 31, 'city': 'New York'}

# Adding key-value pairs
person["email"] = "alice@example.com"
print("Dictionary after adding a key-value pair:", person)  # Output: {'name': 'Alice', 'age': 31, 'city': 'New York', 'email': 'alice@example.com'}

# Removing key-value pairs
del person["city"]
print("Dictionary after removing a key-value pair:", person)  # Output: {'name': 'Alice', 'age': 31, 'email': 'alice@example.com'}

```

## 8. Exception Handling:

_What is exception handling in Python? Provide an example of how to use `try`, `except`, and `finally` blocks to handle errors in a Python script._

Exception handling in Python is a mechanism to handle runtime errors, allowing the program to continue its execution. 

try block: Contains the code that might raise an exception.
except block: Contains the code that runs if an exception occurs in the try block.
finally block: Contains the code that runs no matter what, whether an exception occurs or not.

_Example of usage_
```python

def divide_numbers(a, b):
    try:
        result = a / b
    except ZeroDivisionError as e:
        # Handle division by zero error
        print("Error: Division by zero is not allowed.")
        result = None
    else:
        # This block runs if no exceptions were raised
        print("Division successful.")
    finally:
        # This block runs no matter what
        print("Execution of the 'try' block has finished.")
    
    return result

# Example calls to the function
print(divide_numbers(10, 2))    # Should print the result and success message
print(divide_numbers(10, 0))    # Should handle division by zero error
```

## 9. Modules and Packages:

_Explain the concepts of modules and packages in Python. How can you import and use a module in your script? Provide an example using the `math` module._


A module in is a file containing Python definitions and statements. Modules help organize related functions, classes, and variables into a single file. This makes the code easier to manage and reuse.


A package is a way of organizing related modules into a directory hierarchy. A package is simply a directory with a special `__init__.py` file, which can be empty or can contain initialization code for the package. Packages allow for a hierarchical structuring of the module namespace using dot notation.

_How to import a module_

Using the `import` statement and use its functions, classes, and variables in your script. 

_Example_

```python
import math

# Example usage of the math module

# Calculate the square root of a number
num = 16
sqrt_result = math.sqrt(num)
print(f"The square root of {num} is {sqrt_result}")
```

10. File I/O:

_How do you read from and write to files in Python? Write a script that reads the content of a file and prints it to the console, and another script that writes a list of strings to a file._

_Reading files in Python_

1. Use the open() function with the file path and mode ('r' for reading).
2. Use methods like read(), readline(), or readlines() to access the file content.
3. Close the file using the close() method.

_Example: Reading from a file_
```python
# Specify the file path
file_path = 'sample.txt'

# Open the file in read mode
with open(file_path, 'r') as file:
   # Read the entire content of the file
   file_content = file.read()
   # Print the content to the console
   print("File content:")
   print(file_content)
```

_Writing to a File in Python_

1. Use the `open()` function with the file path and mode (`'w'` for writing).
2. Use the `write()` method to write data to the file.
3. Always close the file using the `close()` method to ensure all data is written.

_Example: Writing to a file_
```python

# List of strings to write to the file
lines_to_write = [
    "Hello,",
    "This is a sample text file.",
    "Writing multiple lines to a file using Python.",
    "End of file."
]

# Specify the file path
file_path = 'output.txt'

# Open the file in write mode
with open(file_path, 'w') as file:
   # Write each line from the list to the file
   for line in lines_to_write:
      file.write(line + '\n')  # Add newline character after each line
print(f"Successfully wrote {len(lines_to_write)} lines to '{file_path}'.")
```