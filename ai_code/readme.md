# PROCview – Custom `my_ps` Command

A C-based implementation that creates a user-defined Linux command `my_ps` by merging process information from `ps aux` and `ps -elf`.

---

## 🚀 Overview

This project focuses on understanding **Linux process management** by combining the outputs of two powerful process-monitoring commands: `ps aux` and `ps -elf`.  
Using system calls and file handling in C, the program extracts relevant process details, merges them, and displays a unified process view similar to standard `ps` utilities.

---

## 🛠️ Key Features

### Custom User Command
Creates a user-defined command `my_ps` that behaves like a native Linux shell command.

### System Command Execution
Uses the `system()` call to execute:
- `ps aux`
- `ps -elf`

### File Handling
Reads and processes command outputs using:
- `open()`, `close()`
- `fscanf()`, `fprintf()`

### Process Information Merging
Combines relevant fields from both command outputs into a single, formatted display.

---

## 📊 Output Description

The output displays a unified view of process information including:

- User ID (UID)
- Process ID (PID)
- Parent Process ID (PPID)
- CPU and Memory usage
- Process state
- Start time
- Command name

This provides a comprehensive snapshot of running processes.

---

## 💻 How to Run

### Compile the Program

```bash
gcc my_ps.c -o my_ps
```

### Execute

```bash
./my_ps
```

## 📈 Learning Outcomes

- Understanding Linux process tables
- Executing shell commands from C
- File-based data extraction and merging
- Creating user-defined Linux commands
- Practical exposure to OS-level utilities

---
