# Course Assessment Tool

The **Course Assessment Tool** is a console-based software application developed in C# using structured programming techniques. Designed for academic environments, it automates the process of conducting multiple-choice question (MCQ) assessments. The application parses question sets from external text files, randomizes the order of question delivery, and records local performance metrics.


## Technical Architecture

The project is built on the .NET Framework and includes the following core artifacts:

* **Target Framework**: .NET Framework v4.7.2
* **Output Type**: Command-Line Executable (.exe)
* **Project File**: `CPLabProject.csproj` manages assembly references and compiler build targets.
* **Source Implementation**: The core application logic is contained within `Program.cs`.


## Key Functionalities

* **File-Driven Initialization**: Dynamically loads quiz pools from system documents without modifying the underlying binary.
* **Algorithmic Randomization**: Utilizes a tracking array technique to display questions in a random order, mitigating academic dishonesty.
* **Bidirectional Traversal**: Supports true session navigation by allowing users to skip forward or go back to previously answered questions during active tests.
* **Persistent Performance Logs**: Appends completion metrics locally to `history.txt`, recording raw scores, calculations, and completion timestamps.


## File Path and Data Layout Constraints

For runtime execution components to bind successfully, your assessment text assets must reside in the target debug build directory:

`D:\Documents\GitHub\Course Assessment Tool\bin\Debug`

The system processes source data files using a strict structural line-count factor. Each question block must consume exactly **six lines** containing no trailing whitespaces or blank spacer records:

1. **Line 1**: Text of the question statement
2. **Line 2**: Option A
3. **Line 3**: Option B
4. **Line 4**: Option C
5. **Line 5**: Option D
6. **Line 6**: Target evaluation key (must evaluate strictly as uppercase `A`, `B`, `C`, or `D`)


### Data Layout Example:

```text
What is the default access modifier for a class in C#?
public
private
internal
protected
C
Usage and Terminal Controls
Launch Methods
The executable file supports both standard deployment and dynamic routing via shell parameters:

Standard Execution: If called without parameters, the interface defaults to searching for an internal Default.txt source file[cite: 4].

Bash
CPLabProject.exe
Parameterized Execution: Pass the file name argument directly to load a targeted test file[cite: 4].

Bash
CPLabProject.exe DataStructuresQuiz.txt
Interactive Navigation Keymap
The terminal environment listens for direct key interception inputs during active assessments:

A / B / C / D

Commits the chosen option to memory for the current question index[cite: 4].

Left Arrow

Moves the cursor back one question position[cite: 4].

Right Arrow

Advances the layout to the next question position[cite: 4].

Escape

Cancels the active testing environment to exit back to the main menu[cite: 4].

Group Assignment Credits
