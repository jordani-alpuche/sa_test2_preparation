📂 CMPS4232 - Test #2 Preparation: Go Project Setup Script

Student Name: Jordani Alpuche
Student ID: 2021255646

Project Overview
This repository contains the Bash shell script, make-go-dir, developed as preparation for CMPS 4232 Test #2. The script automates the setup of a standard directory structure for a Go API project, ensuring consistency and adherence to Go best practices.

🚀 The make-go-dir Script
The make-go-dir script is a utility that creates a project scaffolding, handling argument validation, user confirmation, and essential file initialization.

Prerequisites
To run and test this script, you need:

A Linux environment (e.g., Ubuntu).

Bash shell (default on most Linux systems).

Go installed on your system to test the resulting main.go file.

Usage
The script requires exactly two arguments: the name for the top-level project directory and the identifier for the go.mod file.

Format:

Bash
```
./make-go-dir <ROOT_DIRECTORY_NAME> <IDENTIFIER_NAME>

Example:

Bash

./make-go-dir karpbox umana-amilcar.net
```


📋 Script Execution Flow
The script performs the following steps in sequence:

Argument Check: Verifies that exactly two arguments are provided. If not, it prints a usage message and exits (exit 1).

User Confirmation: Prompts the user to confirm the directory creation. It accepts Y, y, Yes, or yes (case-insensitive) to proceed. Any other input triggers an "Abort." message and a graceful exit (exit 0).

Directory Creation: Creates the specified nested file structure.

File Initialization: Populates the main.go and go.mod files.

Final Message: Provides instructions on how to test the newly created project.

🛠️ Created Directory Structure (Task 1.e)
Upon successful execution, the script creates the following standard Go project structure within the root directory (e.g., karpbox):

```
.
|-- bin          (Directory)
|-- cmd          (Directory)
|   |___ api     (Directory)
|        |___ main.go (File)
|-- internals    (Directory)
|-- migrations   (Directory)
|-- remote       (Directory)
|-- go.mod       (File)
|-- make-file    (File)

```