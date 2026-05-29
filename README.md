# Python - Debugging Strategies

---

Introduction and Context
  
Writing code is only part of programming. Equally important is the ability to understand why code does not behave as expected and to identify the root cause of problems.
  
This process is known as debugging. Debugging involves observing program behavior, collecting evidence, forming hypotheses, and verifying the cause of an issue before applying a fix. Professional developers rarely solve bugs by guessing; instead, they rely on systematic techniques and tools that help them inspect program execution.
  
In this laboratory-style project, you will explore several practical debugging strategies used in Python development. You will work with intentionally faulty programs and investigate how they behave in order to identify and fix the underlying issues.
  
Throughout the tasks, you will practice:
- Reading and interpreting Python error messages and tracebacks
- Inspecting values and program flow
- Using the Python debugger (```pdb```)
- Using logging to observe program behavior
- Following data through multiple functions
- Validating assumptions to detect issues earlier
  
This project is designed as a hands-on debugging lab. The goal is not only to correct the code but also to understand how the bug occurs and how the debugging tools help reveal it.
  
Each task includes a Self-Validation checklist. Use it to confirm that you followed the intended debugging process and covered the learning objectives.
  
The final task of the project is a timed quiz to evaluate your understanding of the debugging strategies explored in this lab.
  
Learning Objectives
  
By the end of this project, you should be able to:
- Explain what debugging is and why it is an essential programming skill
- Interpret Python exceptions and stack traces to locate errors
- Use ```print()``` strategically to inspect program state and execution flow
- Use the Python debugger (```pdb```) to pause execution and inspect variables
- Step through code execution to observe how program state changes
- Trace how incorrect data propagates through multiple functions
- Use the ```logging``` module to record useful runtime information
- Recognize the difference between a symptom of a bug and its root cause
- Apply a structured debugging process rather than trial-and-error changes

---

## 0. Reading the Bug

Objective
  
Learn how to interpret Python error messages and stack traces in order to identify where and why a program fails.
  
Scenario
  
You are given a Python script that crashes when executed. The program attempts to process some data but fails with an exception.
  
Your first responsibility as a developer is not to immediately modify the code, but to understand what the error message is telling you.
  
When a Python program crashes, the interpreter prints a traceback showing:
- the type of error
- the sequence of function calls that led to the error
- the line where the failure occurred
Carefully analyze the traceback and the code before making any changes.
  
Instructions
1. Run the provided script.
2. Observe the error message and traceback.
3. Identify:
    - the type of exception raised
    - the line where the failure occurs
    - the function or part of the program responsible for the error
4. Examine the code around that location.
5. Determine the likely cause of the error.
6. Apply a fix and confirm that the program runs successfully.
  
sample code to debug found in reading.py
  
---

## 1. Debugging with print()
  
Objective
  
Use strategic ```print()``` statements to inspect values and understand how program execution leads to incorrect behavior.
  
Scenario
  
Not all bugs cause a crash. Sometimes a program runs successfully but produces incorrect results.
  
In these situations, developers often begin debugging by temporarily adding ```print()``` statements to inspect:
- input values
- intermediate calculations
- decision points in the code
- unexpected variable states
  
This approach helps reveal where the program begins to behave incorrectly.
  
Instructions
  
1. Run the provided program and observe the incorrect output.
2. Identify the function responsible for producing the result.
3. Add temporary ```print()``` statements to inspect:
    - input parameters
    - intermediate variable values
    - conditional branches
4. Run the program again and analyze the output.
5. Determine where the logic diverges from the expected behavior.
6. Fix the bug.
7. Remove unnecessary debugging prints once the issue is resolved.
  
sample code to debug found in print.py
  
---

# 2. First Steps with `pdb`
  
Objective
  
Use the Python debugger (```pdb```) to pause execution, inspect variables, and step through code.
  
Scenario
  
While ```print() statements can be useful, they are limited. In more complex situations, developers use debugging tools that allow them to pause execution and inspect program state interactively.
  
Python includes a built-in debugger called pdb. It allows you to:
- pause program execution
- inspect variables
- step through code line by line
- continue execution after inspection
  
Instructions
  
1. Identify a suitable location in the provided program to start debugging.
2. Insert a breakpoint using either:
```
breakpoint()
```
or
```
import pdb; pdb.set_trace()
```
3. Run the program.
4. When execution stops, use the debugger commands to explore the program state.
5. Inspect variables involved in the incorrect behavior.
6. Step through the code to observe how values change.
7. Identify the source of the bug.
8. Apply a fix and confirm that the program works correctly.

sample code to debug found in pdb.py
  
---
  
## 3. Following the Data
  
Objective
  
Trace how data flows across multiple functions to locate the origin of a bug.
  
Scenario
  
In many programs, the place where a bug appears is not the place where it originates. Incorrect data may be introduced earlier in the execution and only cause visible problems later.
  
Debugging often requires following the flow of data through multiple functions to determine where the incorrect state first appears.
  
Instructions
1. Run the provided program and observe the incorrect behavior.
2. Identify the function where the incorrect result becomes visible.
3. Trace the origin of the values used by that function.
4. Follow the sequence of function calls that produce the data.
5. Use debugging techniques such as:
    - ```print()``` inspection
    - ```pdb``` stepping
6. Determine where the incorrect value is first introduced.
7. Fix the bug at its true source rather than only addressing the visible symptom.