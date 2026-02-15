## 📝 Implementation Note

This project is **entirely written and implemented manually** by the contributors as part of an academic Operating Systems assignment. No code generators, frameworks, or automated tools were used — all logic, process creation, command execution, file handling, and output merging were designed and coded by hand to understand Linux process management and system calls.

---

# PROCview — Custom `my_ps` Command (Linux Process Viewer)

This project is a Linux-based C application that creates a custom user command called **`my_ps`**, which merges the output of two Linux process inspection commands:

- `ps aux`
- `ps -eLf`

The program demonstrates process creation, output redirection, and file-based merging to generate a combined system process report.

---

## 🚀 Project Overview

The application executes both Linux commands using child processes and redirects their outputs into separate files. These files are then read and merged into a single output file named `merged.txt`, which is finally displayed in the terminal.

The main objective is to understand how system-level commands can be executed and controlled programmatically using Linux system calls.

---

## ✨ Key Features

- Execution of Linux commands using `execlp()`  
- Creation of child processes using `fork()`  
- Output redirection using `dup2()`  
- File handling with low-level and standard I/O functions  
- Automatic merging of command outputs  
- Displays final merged result directly in terminal  

---
