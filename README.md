# PC Virus — Educational Batch Experiments

> ⚠️ **Educational and destructive-code research project.**
>
> This repository contains simple Windows batch-script experiments designed to demonstrate how seemingly small commands can produce disruptive system behavior.
>
> **Do not execute these scripts on your primary computer, production systems, or any machine you do not own or have explicit permission to test.**

## 📌 About

This project was created while learning about:

- Windows batch scripting (`.bat`)
- Command-line execution
- Process behavior
- System startup mechanisms
- Basic destructive malware concepts
- How simple scripts can affect a Windows environment

The examples are intentionally simple. No advanced programming or malware-development knowledge is required to understand the basic concepts.

## 🧪 What You'll Learn

By exploring this repository, you can learn how:

- `.bat` files are created and executed
- Windows commands interact with the operating system
- A script can repeatedly spawn processes
- Commands can trigger system-level actions
- Programs can be configured to run during Windows startup
- Small pieces of code can have significant effects on a system

## 🛠️ Requirements

You only need:

1. A Windows virtual machine or isolated test environment
2. Basic familiarity with Windows
3. A text editor such as Notepad
4. Basic knowledge of the command line

### Recommended Environment

For safety, use an isolated **Windows virtual machine** rather than your everyday computer.

A disposable VM makes it possible to experiment, observe the behavior, and restore the environment using a snapshot afterward.

## 📂 Repository Structure

```text
PCvirus/
├── BootShutdown
├── How Works
└── README.md
```

### `BootShutdown`

Demonstrates how a Windows batch script can trigger a shutdown action and how startup-folder execution can cause a script to run when Windows starts.

### `How Works`

Contains introductory explanations of the concepts behind the examples in this repository.

## 🔬 Concepts Demonstrated

### 1. Fork Bomb

A fork bomb is a program or script that continuously creates new processes.

The basic idea is:

```text
process
 ├── creates another process
 │    ├── creates another process
 │    │    ├── ...
 │    │    └── ...
 │    └── ...
 └── ...
```

As the number of processes increases rapidly, system resources can become exhausted, potentially making the operating system unresponsive.

This is a useful example for understanding:

- Process creation
- Resource exhaustion
- Recursive execution
- Denial-of-service concepts

### 2. Destructive File-System Commands

Windows command-line utilities can perform powerful file-system operations.

Some commands can recursively delete files or otherwise modify data on a drive. This demonstrates why command-line tools should be treated carefully, especially when running scripts with elevated privileges.

> **Do not experiment with destructive commands on real data.**

## ▶️ How Batch Files Work

Windows batch files use the `.bat` extension and contain commands that Windows executes sequentially.

A basic batch file can be created with Notepad:

1. Open **Notepad**.
2. Write a batch command.
3. Select **File → Save As**.
4. Change **Save as type** to `All Files`.
5. Give the file a `.bat` extension.
6. Execute it inside your isolated test environment.

For destructive experiments, use a disposable VM and take a snapshot before testing.

## ⚠️ Safety Warning

Some concepts demonstrated by this project can cause:

- System instability
- Excessive CPU or memory usage
- Forced shutdowns
- Loss of unsaved work
- File or data deletion

**Never run destructive scripts on:**

- Your primary computer
- Production machines
- Shared systems
- Another person's computer
- Systems containing important data

Only perform experiments in an environment where you have explicit authorization.

## 🎯 Purpose

This project is intended for **education and experimentation**, not for harming systems.

Understanding how simple commands can produce disruptive behavior is useful when learning:

- Windows internals
- System administration
- Malware analysis
- Defensive security
- Incident response
- Endpoint security
- Command-line security

## 🚧 Project Status

This is a beginner-level educational project.

Future additions may include safer demonstrations of:

- Process management
- Windows command execution
- Batch scripting techniques
- Persistence concepts
- Malware-analysis methodology
- Detection and mitigation techniques

## 📜 Disclaimer

The author is not responsible for damage, data loss, system instability, or other consequences resulting from misuse of the material in this repository.

**Use only in controlled environments and only on systems you are authorized to test.**

---

**Learn how it works. Break it safely. Understand how to defend against it.**
