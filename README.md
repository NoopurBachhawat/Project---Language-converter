# Project---Language-converter
This project converts Python code into C using AST parsing. It reads Python input, analyzes its structure, and translates basic constructs like variables, loops, conditions, and print statements into equivalent C syntax, generating readable output code automatically.




🔹 Introduction

This project is a Python to C code converter developed using Python. It translates basic Python programs into equivalent C programs automatically. The system uses the concept of Abstract Syntax Tree (AST) to analyze Python code structure and generate corresponding C syntax.

Python is a high-level, dynamically typed language, whereas C is a low-level, statically typed language. Due to these differences, direct conversion is complex. This project focuses on converting structured and basic Python constructs into C.




🔹 Objective
To design a system that converts Python code into C code
To understand compiler design concepts like parsing and translation
To automate code conversion for basic programming constructs
To reduce manual effort in rewriting code from Python to C




🔹 Working of the Project
The project works in the following steps:
1. Input Phase
User enters Python code manually in the terminal (or file).

2. Parsing Phase
The Python code is parsed using the built-in ast module
It converts the code into a tree structure (AST)

3. Processing Phase
The program traverses the AST
Each Python construct is identified (like variables, loops, conditions)

4. Conversion Phase
Python syntax is mapped to equivalent C syntax
Example:
print() → printf()
for range() → for loop
if → if

5. Output Phase
Generated C code is displayed
Also saved in a .c file




🔹 Features
✅ Converts variable assignments
✅ Supports arithmetic operations (+ - * /)
✅ Converts print() to printf()
✅ Supports if-else conditions
✅ Converts for loops (range)
✅ Generates structured and readable C code
✅ Saves output automatically




🔹 Limitations
❌ Does not support advanced Python features
❌ No support for:

Classes & OOP
Libraries (NumPy, Pandas)
Dynamic typing fully
Complex functions

👉 Because Python and C are fundamentally different languages.




🔹 Applications
Educational tool for learning language differences
Helps beginners understand Python vs C syntax
Useful in compiler design learning
Can be extended into a mini-compiler




🔹 Technologies Used
Python (Main language)
AST (Abstract Syntax Tree)
VS Code (IDE)




🔹 Conclusion
The Python to C converter successfully demonstrates how high-level language constructs can be translated into low-level language syntax using parsing techniques. Although it supports only basic features, it provides a strong foundation for understanding code translation and compiler design concepts.
<img width="1733" height="819" alt="Screenshot 2026-03-26 100627" src="https://github.com/user-attachments/assets/5f1ed7f2-5aeb-429b-bf82-d0f4fca5f372" />
<img width="1728" height="801" alt="Screenshot 2026-03-26 100600" src="https://github.com/user-attachments/assets/5292147c-8f92-4beb-9ce8-81d0465f83b3" />
