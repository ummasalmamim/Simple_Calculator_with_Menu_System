# Simple Calculator with Menu System

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python 3.x">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter Notebook">
  <img src="https://img.shields.io/badge/Interface-Command%20Line-4D4D4D?style=for-the-badge&logo=gnometerminal&logoColor=white" alt="Command-line interface">
</p>

A console-based arithmetic calculator written in Python and presented as a Jupyter Notebook. The program accepts two numbers from the user and provides a numbered menu through which six arithmetic operations can be performed repeatedly until the user chooses to exit.

<p align="center">
  <img src="images/demo.png" alt="Simple Calculator running in the terminal" width="560">
</p>

---

## Table of Contents

- [Overview](#overview)
- [Built With](#built-with)
- [Features](#features)
- [Supported Operations](#supported-operations)
- [Requirements](#requirements)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Sample Session](#sample-session)
- [Program Structure](#program-structure)
- [Error Handling](#error-handling)
- [Known Limitations](#known-limitations)
- [Possible Enhancements](#possible-enhancements)
- [Author](#author)

---

## Overview

This project demonstrates fundamental Python programming concepts, including:

- Reading and converting user input (`input()`, `float()`)
- Indefinite iteration with a `while True` loop
- Conditional branching with `if` / `elif` statements
- Loop control with `break` and `continue`
- Basic input validation and defensive checks against invalid arithmetic

The two operands are entered once at the start of the program. The menu is then displayed repeatedly, allowing the user to apply different operations to the same pair of numbers.

---

## Built With

<p align="left">
  <a href="https://www.python.org/"><img src="https://skillicons.dev/icons?i=python" alt="Python" width="48" height="48"></a>
  &nbsp;
  <a href="https://jupyter.org/"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original-wordmark.svg" alt="Jupyter" width="48" height="48"></a>
</p>

| Technology                              | Purpose                                                   |
|-----------------------------------------|-----------------------------------------------------------|
| [Python](https://www.python.org/)       | Programming language used to implement the calculator     |
| [Jupyter Notebook](https://jupyter.org/) | Environment used to write, run, and present the program  |

---

## Features

- Interactive, menu-driven command-line interface
- Six arithmetic operations on floating-point numbers
- Continuous operation until the user explicitly selects **Exit**
- Protection against division and modulus by zero
- Validation of menu selections with an informative message for invalid choices
- Clearly delimited result output for readability

---

## Supported Operations

| Option | Operation      | Expression        | Notes                                   |
|:------:|----------------|-------------------|-----------------------------------------|
| 1      | Addition       | `num1 + num2`     |                                         |
| 2      | Subtraction    | `num1 - num2`     |                                         |
| 3      | Multiplication | `num1 * num2`     |                                         |
| 4      | Division       | `num1 / num2`     | Rejected when the second number is zero |
| 5      | Modulus        | `num1 % num2`     | Rejected when the second number is zero |
| 6      | Power          | `num1 ** num2`    |                                         |
| 7      | Exit           | —                 | Terminates the program                  |

---

## Requirements

- **Python** 3.x
- **Jupyter Notebook** or **JupyterLab** (alternatively, Google Colab or VS Code with the Jupyter extension)

No third-party libraries are required.

---

## Getting Started

1. **Clone the repository**

   ```bash
   git clone https://github.com/ummasalmamim/Simple_Calculator_with_Menu_System.git
   cd Simple_Calculator_with_Menu_System
   ```

2. **Launch Jupyter**

   ```bash
   jupyter notebook
   ```

3. **Open** `Simple_Calculator_with_Menu_System_.ipynb` and run the code cell.

Alternatively, the notebook can be opened directly in [Google Colab](https://colab.research.google.com/) via **File → Open notebook → GitHub** by entering the repository URL.

---

## Usage

1. Enter the **first number** when prompted.
2. Enter the **second number** when prompted.
3. Select an operation by entering a number from **1** to **7**.
4. The result is displayed, and the menu reappears.
5. Repeat step 3 as needed, or enter **7** to exit.

---

## Sample Session

The following output was produced with the inputs `100` and `0`:

```text
Enter the first number: 100
Enter the second number: 0

===== Simple Calculator =====

_____ Menu _____
1. Addition
2. Subtraction
3. Multiplication
4. Division
5. Modulus
6. Power
7. Exit
Enter your choice (1-7): 1
=======================
Result: 100.0
=======================

Enter your choice (1-7): 4
=====================
Error: Division by zero is not allowed.
=====================

Enter your choice (1-7): 6
========================
Result: 1.0
=========================

Enter your choice (1-7): 7
Calculator closed. Thank you!
```

*(Repeated menu listings have been omitted for brevity.)*

---

## Program Structure

```text
Simple_Calculator_with_Menu_System/
├── Simple_Calculator_with_Menu_System_.ipynb   # Calculator source code and sample output
├── images/
│   └── demo.png                                # Screenshot of a sample session
└── README.md                                   # Project documentation
```

The program logic proceeds as follows:

1. Read two numbers and convert them to `float`.
2. Enter an infinite loop that displays the menu.
3. Read the user's choice and execute the corresponding operation.
4. If the choice is `7`, print a closing message and terminate the loop.
5. If the choice is not between `1` and `7`, display an error message and redisplay the menu.

---

## Error Handling

| Condition                               | Program Response                                   |
|-----------------------------------------|----------------------------------------------------|
| Division with a second number of zero   | `Error: Division by zero is not allowed.`          |
| Modulus with a second number of zero    | `Error: Modulus by zero is not allowed.`           |
| Menu choice outside the range 1–7       | `Invalid choice! Please choose from 1 to 7.`       |

---

## Known Limitations

- The two operands are entered only once; changing them requires restarting the program.
- Non-numeric input for the operands (for example, `abc`) raises a `ValueError` and stops the program, as no exception handling is currently in place.
- Very large exponents in the **Power** operation may produce an `OverflowError`.

---

## Possible Enhancements

- Allow new operands to be entered for each calculation.
- Wrap numeric input in `try` / `except` blocks to handle invalid entries gracefully.
- Refactor each operation into a dedicated function to improve modularity and readability.
- Add further operations such as square root, floor division, and percentage.
- Provide a standalone `.py` script for execution outside Jupyter.

---

## Author

**ummasalmamim**
GitHub: [@ummasalmamim](https://github.com/ummasalmamim)

Developed as a Python programming exercise.
