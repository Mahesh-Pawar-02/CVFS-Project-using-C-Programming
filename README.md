# Customised Database Management System

This project is a Customised Virtual File System (CVFS) implemented in C Programming. It provides a simplified and user-friendly interface for file operations, supporting various functionalities such as creating, reading, writing, listing, and deleting files.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Usage](#usage)
- [Commands](#commands)
- [Compilation and Execution](#compilation-and-execution)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The Customised Database Management System simulates a virtual file system where users can create and manage files with different permissions. It maintains an in-memory representation of files and supports basic file operations.

## Features

- Create new regular files with specific permissions
- Read from and write to files
- List all files with their metadata
- Display detailed information about files
- Delete files
- Change file offset for reading and writing
- Close specific or all open files
- Remove data from files

## Usage

To use the Customised VFS, follow these steps:

1. Compile the code.
2. Run the executable.
3. Use the provided commands to interact with the file system.

## Commands

- `ls` : List all files
- `create <FileName> <Permission>` : Create a new file with specified permission
- `open <FileName> <Mode>` : Open an existing file
- `read <FileDescriptor> <NoOfBytes>` : Read data from a file
- `write <FileDescriptor> <Data>` : Write data to a file
- `stat <FileName>` : Display information of a file using file name
- `fstat <FileDescriptor>` : Display information of a file using file descriptor
- `close <FileName>` : Close a specific file
- `closeall` : Close all open files
- `truncate <FileName>` : Remove data from a file
- `rm <FileName>` : Delete a file
- `lseek <FileDescriptor> <Size> <StartPoint>` : Change the offset of a file
- `man <CommandName>` : Display user manual for a specific command
- `clear` : Clear console
- `exit` : Terminate the file system

## Compilation and Execution

To compile and run the project, use the following commands:

```sh
gcc Customised_Database_Management_System.c -o vfs
./vfs
