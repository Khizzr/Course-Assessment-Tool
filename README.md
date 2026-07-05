The Course Assessment Tool is a lightweight, console-based application built in C# using structured programming concepts. It allows students to test their academic knowledge or skills by running customized multiple-choice question (MCQ) tests. The program automatically randomizes question delivery, tracks performance, and stores a historical log of test results.

🚀 Features
Custom MCQ Loading: Reads questions directly from text files.

Question Randomization: Randomizes the order of questions each time a quiz begins to ensure a unique, fair testing experience.

Interactive Navigation: Allows users to skip forward to the next question or backtrack to review/change previous answers.

Performance Analytics: Instantly calculates the number of correct/incorrect answers and presents a final percentage score.

Persistent Score History: Automatically logs quiz history (including dates and timestamps) to a local file, which can be viewed or deleted via the menu.

📂 Setting Up Your Custom MCQs
To load your own quizzes into the software, you must place or update the quiz text files inside the build directory:
D:\Documents\GitHub\Course Assessment Tool\bin\Debug

Text File Format Requirements
The system parses files using a strict 6-line-per-question rule. Each question block inside the file must follow this exact order:

Line 1: The Question statement

Line 2: Option A

Line 3: Option B

Line 4: Option C

Line 5: Option D

Line 6: The Correct Answer key (Capital letter: A, B, C, or D)

Example File Structure (Default.txt):
Plaintext
What is the default access modifier for a class in C#?
public
private
internal
protected
C
Which of the following is a value type in C#?
string
int
class
interface
B
⚠️ Important Note: Make sure there are no trailing blank lines at the very bottom of your text files, as the program relies on exact multiples of 6 lines to accurately map questions and answers.

🛠️ How to Run the Application
1. Default Mode
By default, running the executable will look for a file named Default.txt inside the bin\Debug directory.

Bash
CPLabProject.exe
2. Custom Quiz Mode (Command-Line Argument)
If you want to run a specific quiz file (e.g., MidtermPrep.txt), pass the file name as a command-line argument:

Bash
CPLabProject.exe MidtermPrep.txt

Navigation Controls
When a quiz is active, use the following interactive console keys:

A, B, C, or D — Select your answer.

Right Arrow (->) — Advance to the next question.

Left Arrow (<-) — Return to the previous question.

Esc — Abandon the quiz and return to the Main Menu.

Developed as part of the Computer Programming Lab Project
