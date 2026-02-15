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
## 🧠 Core Concepts

## ⚙️ Program Execution Flow

1. Parent process creates `x1.txt`.  
2. Child process executes `ps aux` and writes output to `x1.txt`.  
3. Parent waits for child completion.  
4. Parent creates `x2.txt`.  
5. Another child executes `ps -eLf` and writes output to `x2.txt`.  
6. Parent opens both files and reads their contents.  
7. Data is merged into `merged.txt` with proper headings.  
8. Final merged file is displayed using `cat merged.txt`.

---

## 📂 File Handling Strategy

The program uses:

- `open()` / `close()` for file descriptors  
- `fopen()` for reading/writing streams  
- `fgetc()` and `fputc()` for copying file contents  
- `fprintf()` for formatted output  

---

## 📊 Learning Outcomes

- Understanding Linux process creation and execution  
- Output redirection using file descriptors  
- Executing shell commands from C programs  
- Managing parent–child synchronization  
- Merging multiple command outputs using file handling  

---

## ⚠️ Limitations

- **Sequential Execution:** Commands are executed one after another instead of concurrently.  
- **Temporary Files:** Intermediate files (`x1.txt`, `x2.txt`) are required before merging.  
- **No Filtering:** The merged output contains complete command outputs without processing.  
- **Basic Error Handling:** Minimal checks for file or execution failures.  

---

## 👤 Contributors

1. Bharath Reddy  
2. Aman Das  
3. Samam Roy  
4. Saumya Kumari  
5. Rinika Banarjee  
6. Pedenla Bhutia  
7. Sruthi Vaddadhi  
8. Anay Bhattacharya (Group Leader)  
9. Dhrub Sah
