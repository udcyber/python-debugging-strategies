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

code found in reading.py

