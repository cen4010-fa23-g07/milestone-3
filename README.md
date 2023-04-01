
# Milestone 3 Project "Clever Calc"

## Table of contents

1. [Executive Summary](#executive-summary)
2. [Competitive Analysis](#competitive-analysis)
3. [Data Definition](#data-definition)
4. [Overview, Scenarios, Use-Cases](#overview-scenarios-and-use-cases)
5. [High-Level Functional Requirements](#high-level-requirements)
6. [List of Non-Functional Requirements](#list-of-non-functional-requirements)
7. [High-Level System Architecture](#high-level-system-architecture)
8. [Team](#team)
9. [Checklist](#checklist)

## Executive Summary

The project name is Clever Calc, a Math utility designed to help aid students in learning how to solve algebraic equations in the terms of a desired variable. The user enters an equation they would like to solve. If the equation is valid, the program will ask for a variable for which the equation is to be solved or for which the equation is to be put in terms. The equation solver will then ‘solve’ the equation, printing out each step it performs as it functions. When the solution is reached, the student will have a step by step instructions on how to solve that equation. Additionally, the software can be paused at any point in the solution path to allow the student to figure out the problem on their own. This software may also solve simple systems of equations if it is needed. Tools of a similar caliber already exist on the market, but often come with one or more of three caveats. Programs either solve the equation through approximation or brute force, don’t provide specific instructions to the user, or charge users a membership fee to view the solution. In regards to the last caveat, even those programs, which display the necessary solution, only show the raw changes in the equations. Not specifying the exact method of each step. Our project acts as a training utility. Students can enter training mode, in which the student will tell the program what the next step in solving the equation is. The program will correct any errors and then continue to the next step. Our software will run completely offline as an executable file, but more importantly, will be included as a C++ source-code library. In short, this allows other educational software designers to implement our tool as part of their learning software.

## Competitive Analysis

|                 | Step-by-Step Solutions? | Offline use? | Software integration? | Pausable solutions? | Guided learning? | Practice mode? |
| --------------- | ----------------------- | ------------ | --------------------- | ------------------- | ---------------- | -------------- |
| **Keisan**      | No.                     | No.          | No.                   | No.                 | No.              | No.            |
| **Wolfram**     | Only with Premium.      | Yes.         | Yes.                  | No.                 | No.              | No.            |
| **Symbolab**    | Yes.                    | No.          | No.                   | No.                 | No.              | No.            |
| **Our Product** | Yes.                    | Yes.         | Yes.                  | Yes.                | Yes.             | Yes.            |

Our product will do everything our competitors' products can do and more. All of these products can solve equations step-by-step, but ours gives users reasoning for which steps have been taken, as well as the ability to pause during solving. The ability to pause allows users to finish the rest of the problem on their own, even if they were stuck on one part. Users can also engage in practice mode, where the application generates a linear equation, and then the user enters their answer to see if they were correct. Our product will also feature easy plotting -- all that is needed to do is save the equation and use the plotting functionality, while our competitors' products force users to go to another page. Our product also includes software integration, meaning that it can be included in other programs if desired.

## Data definition

**Algebra** - The expression of problems as math equations.  
**Linear Equation** - Equation in terms of one variable with only a coefficient and constant.  
**Variable** - An placeholder for numeric data, to be filled in by the user or solved by the program’s algorithm.  
**Software Library** - A set of code designed to be incorporated into and compiled with user software.  
**Command line** - A developer-focused application that can be used to execute programs whilst providing a syntax to provide those same programs with parameters and options.  
**Memory** – Storing solved math equations (for later usage if needed).  
**Consumer** - Actor who uses the application to solve or plot linear equations.  
**Developer** - Actor who integrates the application library into their program.  
**Plot** - To plot points on a graph to display a linear equation being graphed.  
**Account** - Storing previous work or suggesting the user's preference.  
**Support** - Actor who helps a consumer in need of usage towards the program.  
**Favorable** - Suggest common problems to users after many similar equations are presented.  
**Solve/Explain** - To move on to the next step of the equation with an explaination as to why it is.  

## Overview, scenarios, and use-cases

The primary usage of our software will be through the user interface, where a student (our user, in this case) will use the program to learn the steps required to solve linear equations. The prospective student will open up our software, and select the solving mode. Our student wishes to learn how to solve a linear equation. So, the student selects the linear equation mode and enters the linear equation. If any errors were made, our software reminds the student to correct, them and then proceed. Once ready, the student can pick their desired operation mode. We suspect that the step mode will be very popular. The student clicks each step and reads very carefully. They study each step and make sure to understand how to solve their math equations with better confidence. Once the student feels ready, they can activate quiz mode, and then test themselves against the computer. If the student, teacher, or parent wants to see the progress they're making, the stats will always be saved.

Additionally, the code can also be used as a library: If a developer needs a simple and efficient library to compute and solve linear equations, he or she can import the code onto their project(s), and make use of the simple library provided. There are three main ways in which the project can be used:

1. The developer makes use of it as a library: By importing the C++ code as a library to their project(s), developers can take advantage of the preexisting code written in this project. Using a simple and comprehensive API, they can proceed to use it to solve linear equations as an embedded system. After importing the library, the developer can have access to the methods and functions, which he or she can then invoke and compose to accomplish his or her goals.
    * A school system wishes to set up lab time for their students to practice math problems, without giving them access to the internet. The developer they hire to make this application simply needs to include the library for our product into their application, rather than developing new functionality for linear equation solving.
2. The program can be invoked from the command line: By executing a specific command on the command line, developers or consumers can quickly gain access to the tool. Using the interactive menu, the consumer can choose from a list of useful options and decide what operation they would like to perform, be it solving linear equations or creating a simple visual graph.
    * A student wishes to get better at solving linear equations. The student can input their equations and then enter training mode, allowing them to solve up to a certain point if they get stuck, and then continue the equation on their own. The student can also use practice mode to get new problems and then check their answers.
    * An engineer has solved two systems of linear equations and wishes to plot them for further analysis. The engineer only needs to save the systems after solving and then will be able to use the graphing functionality to see them for comparison.
3. While in use of the program, the consumer can be prompted if they would like a similar problem presented to them in a different linear equation format than what the consumer presented. This way, the student can excel on a given topic of mathematics for them to understand on a deeper level.
    * A student wanting to practice more problems than the one assigned to better achieve a full understanding of a certain type of question.


## High level requirements
### Priority 1: Must-Haves
1. Set usage functionality (linear equation, a system of equations, etc)
    - Set the program functionality for different types of equations.
    - Base options will include linear equations and systems of equations.
    - Chosen via a selection menu, the default will be linear equations.
    - Future functionality may include limits, derivatives, and integrals.
2. Enter the equation.
    - The user will type the equation using variables, one equality operator, and various required operator symbols.
    - In a system of equations, the user will enter multiple equations.
    - Once our equations are valid, the user may select a solve mode.
3. Solve mode.
    - Several solve modes are included and can be chosen by the user.
    - Instant mode: Once activated, the entire solution and required steps are revealed to the user.
    - Step mode: Reveals one step of the solution to the user after each activation.
    - Quiz mode: Prompts the user for the next step towards the solution, and checks for accuracy.
    - Practice mode: Generates random linear equations for the user to solve, then allows them to check their answer.
4. Source-code Library
    - All essential functions of the software will be available as a C++ source-code library.
    - Usage of all primary functions, including the usage type, equation solving, and history/retrieval will be available.
    
### Priority 2: Desired
1. Plotting
    - Ask the user if the linear expression needs to be graphed for visual understanding.
2. History
    - Each equation is stored in the history, for the user to revisit.
    - Over time old solutions are culled.
    - User accuracy in the quiz mode will be saved to the user's stats. This can be cleared at any time.
3. Stats
    - Shows statistic on what the type of questions user is best at
    - Shows statistic on what the most failed types of questions are
4. Adding
    - Gives user option to add specific equation to their history 

### Priority 3: Opportunistic
1. More Example Mode
    - User prompted if they would like more similar questions to their functionality.
    - Randomizes numbers from the user's first input onto the next question.
2. Non-Registered Member
    - User is given the option to register for an account which would allow for **4.History** to be possible.
    - User is prompted to input a valid email address and password **(Must meet criteria of at least 1 capital letter, symbol, numbers)**.
    - User may also have the option to register via google account.
3. Registered Member
    - User prompted to enter login credentials **(email address and password)**.
    - Given access to **4.History**
4. Update
    - User is given the option to update their account password,username or email
    - Restrictions on user to make sure the password isn't the same as previous password/s.
5. Delete
    - User is given option to delete their account.  

## List of non-functional requirements.

1. Performance
    - Must be fast and demonstrate consistent performance.
    - Usage of appropriate Data structures and algorithms where needed.
2. Library
    - Importable and usable as a C++ library.
3. Desktop compatible
4. 24/7 usage uptime
5. Usability
    - To be able to use a relatively understandable interface.
    - Should be straightforward to understand.
    - Should produce comprehensive results that are easy to digest.
6. Maintenance
    - A lot of debugging, testing, and overall modifications implemented onto our product.
    - Usage of best code practices.
7. Fault tolerance
    - The application will inform the user if the equation is unsolveable.
    - The application will inform the user if something within the system has failed.
    - The application should not cause undefined behavior under any user input.


## High-level system architecture

**Languages:** C++, Python  
**Tools:** g++, Visual Studio/Visual Studio Code, Git

The tooling is straightforward and traditional. C++ will be the main programming language employed for the implementation of the project, with Python being used for more specific purposes such as the Graphing feature, whereas C++ will be used for the general-purpose programming of the project. The C++ version used would be a modern one, C++17 or above to make use of the latest features provided by the C++ standard and its compilers. No build tool (ex. CMake) will be used for the project since the project structure will be relatively straightforward.

Main database tables:
1. User (contains username, password, userid)
2. Equations (contains problemid, equation(s), solution(s))
3. History (contains userid, problemid)

Media (e.g. images used for the front end) will be kept in the filesystem.

Search/filter architecture:

APIs:

Non-trivial algorithms:
- The application will give the user the option to generate a new (set of) equation(s) based on their current entries. The application will do this by randomizing the user's input into the new equation, but it will also need to be verified as solveable and not too difficult. To do this, the algorithm will first attempt to solve the generated equation without showing the user. If it is successful, it will then check the number of steps it took to solve it, and will present it to the user if the number of steps is similar to the user's original problem. Else, it will attempt to generate a new equation.

## High-Level UML Diagrams

![image](https://user-images.githubusercontent.com/124008459/229259686-1f2a2721-4f02-4360-899e-e0628ecc37e4.png)


## Key Risks

Risk: Many team members have term projects coming up, in addition to this one.  
Solution: Assign each team member what they should be coding as early as possible in order to allow them to prioritize their time.

## Team

Scrum Master  
- Dante Ricketts

Product Owner  
- Yurixander Ricardo Silva

Developers  
- Clinton Hoang
- Lauren Morlock
- Zee Fisher

## Checklist

1.  Team decided on basic means of communications: **Done.**
2.  Team found a time slot to meet outside of the class: **Done.**
3.  Front and back-end team leads chosen: **Done.**
4.  Github master chosen: **Done.**
5.  Team ready and able to use the chosen back and front-end frameworks: **Done.**
6.  Skills of each team member defined and known to all: **Done.**
7.  Team  lead  ensured  that  all  team  members  read  the  final  M1  and agree/understand it  before submission: **Done.**
