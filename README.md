# Unreal Python Sudoku Solver
### Unreal Engine <-> Python Interface
Sudoku solver written in Python that interfaces with Unreal Engine for the GUI.

In this team project, we created a Python script to generate and solve sudoku puzzles. It does this by using constrained back-propogation algorithms. But we needed a user interface. I used Unreal Engine and created a sudoku puzzle class and made a simple script that solved the puzzle with a brute force algorithm (significantly slower that the Python script, for effect). Instead of translating the Python code to C++, I used Rama's plugin that allows for OS process creation and created an interface between Unreal Engine and Python. This is the call to Python that is run in a new process:
```
"from sudoku1 import *; v = generate( [variable_from_unreal_engine] ); tofile('input.txt', v); solve([v])"
```
The semicolons actually execute the command up until that point (which I certainly didn't know about the command line and Python).

*While this is really cool in my opinion, the applications are probably limited. It's slow and relies on the transfer of strings between Unreal Engine and Python. However it handles this small proof of concept example very well.*


#### The part of the Unreal Engine script that interfaces with the Python script:
<p align="left">
  <img src="interface.png" width="800">
</p>

#### The brute force method of solving the puzzle:
<video width="640" height="480" controls preload="none">
  <source src="sudoku-brute.mp4" type="video/mp4" preload="none">
  <a href="https://ryanawalters.github.io/UnrealPythonSudokuSolver/"><b>Please view this page with videos enabled!</b></a>
</video>

#### The back propogation method of solving the puzzle using the Python script:
<video width="640" height="480" controls preload="none">
  <source src="sudoku-brute.mp4" type="video/mp4" preload="none">
  <a href="https://ryanawalters.github.io/UnrealPythonSudokuSolver/"><b>Please view this page with videos enabled!</b></a>
</video>
