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






🔹 Detailed Working of the Project

The Python to C Language Converter works as a structured translation system that converts high-level Python code into equivalent C code using Abstract Syntax Tree (AST) parsing. The entire process is divided into multiple phases, each responsible for a specific task in the conversion pipeline.

🔸 1. Input Phase

In this phase, the user provides Python code as input. The input can be given either through the terminal or by reading from a file. This code serves as the source program that needs to be converted into C language.

🔸 2. Parsing Phase

The input Python code is parsed using Python’s built-in ast module. This module converts the source code into an Abstract Syntax Tree (AST), which is a structured tree representation of the program.

Instead of treating code as plain text, AST represents the logical structure of the program in terms of nodes such as assignments, loops, conditions, and function calls.

🔸 3. AST Generation

Once parsing is complete, the Python code is transformed into a tree-like structure. Each node in the tree represents a specific construct of the program.

For example:

Assignment statements become Assign nodes
Loops become For nodes
Conditions become If nodes
Function calls like print() become Call nodes

This structured representation makes it easier to analyze and translate the code.

🔸 4. AST Traversal

After generating the AST, the program traverses the tree using a visitor-based approach. A custom class (usually derived from ast.NodeVisitor) is used to visit each node in the tree.

Each type of node is handled by a specific function such as:

visit_Assign() for variable assignments
visit_For() for loops
visit_If() for conditional statements
visit_Call() for function calls

During traversal, the program identifies the type of construct and extracts relevant information required for conversion.

🔸 5. Conversion Phase

In this phase, Python constructs are mapped to their equivalent C syntax. The conversion is rule-based and depends on the type of node encountered.

Examples of conversion:

Variable Assignment
Python: x = 10
C: int x = 10;
Print Statement
Python: print(x)
C: printf("%d\n", x);
For Loop
Python: for i in range(5):
C: for(int i = 0; i < 5; i++)
If Condition
Python: if x > 5:
C: if(x > 5) {

Since Python is dynamically typed, the converter assumes default data types (usually int) for variables.

🔸 6. Code Generation

After converting each construct, the program combines all translated parts to generate complete C code. It also adds necessary boilerplate code such as:

#include <stdio.h>
int main() function
Proper braces and indentation

The final output is structured and readable C code.

🔸 7. Output Phase

The generated C code is displayed on the screen and also saved automatically into a .c file. This allows the user to compile and run the code using a C compiler.

🔹 Internal Design and Implementation

The project is implemented using a class-based approach where a custom visitor class is created by extending ast.NodeVisitor.

Each method in the class is responsible for handling a specific type of AST node. The methods extract necessary details from nodes and append the corresponding C code into an output string.

This modular design makes the system easy to extend and maintain.

🔹 Key Concepts Used
Abstract Syntax Tree (AST)
Parsing and Traversal
Compiler Design Basics
Syntax Mapping between Programming Languages
Code Generation Techniques
🔹 Challenges in the Project

The main challenge in this project arises due to the fundamental differences between Python and C:

Python is dynamically typed, while C is statically typed
Python handles memory automatically, while C requires manual handling
Python syntax is simple, whereas C syntax is strict

Because of these differences, not all Python programs can be directly converted into C.

🔹 Limitations of the System
Does not support object-oriented programming (classes and objects)
Cannot handle external libraries like NumPy or Pandas
Limited support for complex functions and recursion
Assumes fixed data types (mostly integers)
Does not fully support dynamic typing
🔹 Future Improvements
Support for more data types (float, char, string)
Handling user-defined functions
Support for arrays and pointers
Extending to full compiler-level translation
Adding GUI for better user interaction
🔹 Conclusion (Detailed)

The Python to C converter demonstrates how high-level programming constructs can be translated into low-level language syntax using parsing techniques. By utilizing Abstract Syntax Trees, the project efficiently analyzes and processes Python code structure.

Although the system supports only basic constructs, it provides a strong foundation for understanding compiler design, syntax translation, and program analysis. With further enhancements, this project can evolve into a more advanced code translation tool or even a full-fledged compiler.
