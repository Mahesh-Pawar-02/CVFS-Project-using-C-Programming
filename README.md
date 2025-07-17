# 🗃️ Customised Virtual File System (CVFS)

A simulated Virtual File System (VFS) implemented in C/C++ that replicates basic functionalities of Unix-like file systems. This project demonstrates core OS concepts like inode structure, file permissions, command parsing, and memory management, all from scratch — without relying on the actual OS file APIs.

---

## 🚀 Features

- 📄 Create, open, read, write, and delete regular files.
- 🔐 Permission management (Read / Write / Read+Write).
- 📊 File metadata viewing (`stat` and `fstat`).
- 📂 List files (`ls`) with inode details.
- 🧹 Truncate file contents (`turncate`).
- 🎯 File pointer manipulation (`lseek`).
- 👨‍💻 Interactive shell interface for command input.

---

## 🧠 Core Concepts Implemented

- **Inode Table (DILB)** for file metadata.
- **User File Descriptor Table (UFDT)** simulating file descriptors.
- **Superblock** to track total/free inodes.
- **FileTable** to manage opened file sessions.
- **Manual Command Parser** using `sscanf()`.

---

## 🛠️ Installation & Usage

### 🧾 Compile the Program

```bash
g++ VFS.cpp -o vfs
```

### ▶️ Run the Virtual File System

```bash
./vfs
```

> You'll enter an interactive CLI environment resembling a Unix shell.

---

## 💡 Available Commands

| Command | Usage | Description |
|--------|--------|-------------|
| `create` | `create <filename> <permission>` | Create a new file with read/write permissions |
| `open` | `open <filename> <mode>` | Open an existing file |
| `read` | `read <filename> <size>` | Read bytes from a file |
| `write` | `write <filename>` | Write data to a file (prompts for input) |
| `ls` | - | List all files |
| `stat` | `stat <filename>` | Display metadata of a file |
| `fstat` | `fstat <fd>` | Display metadata using file descriptor |
| `lseek` | `lseek <filename> <offset> <start/cur/end>` | Move file pointer |
| `close` | `close <filename>` | Close a specific file |
| `closeall` | - | Close all open files |
| `rm` | `rm <filename>` | Delete a file |
| `turncate` | `turncate <filename>` | Erase file contents |
| `help` | - | List all available commands |
| `man` | `man <command>` | View manual for specific command |
| `clear` | - | Clear screen (may not work on all terminals) |
| `exit` | - | Terminate the VFS shell |

---

## 🔐 Permissions Guide

| Value | Permission |
|-------|------------|
| `1` | Read Only |
| `2` | Write Only |
| `3` | Read and Write |

---

## 📦 File System Limits

- Max files (inodes): **50**
- Max file size: **2048 bytes**
- File name limit: **50 characters**
- Max open files: **50**

---

## 📸 Sample Session

```
Customised VFS : > create demo.txt 3
File successfully created with file descriptor: 0

Customised VFS : > write demo.txt
Enter the data:
This is a test string.

Customised VFS : > read demo.txt 100
This is a test string.

Customised VFS : > ls
File Name    Inode No    File Size    Link Count
demo.txt     1           22           1

Customised VFS : > stat demo.txt
File name : demo.txt
Inode No  : 1
File Size : 2048
Actual Size : 22
Permission : Read & Write
```

---

## 📚 Project Purpose

This VFS is an academic/systems programming project aimed to:

- Understand low-level file system internals.
- Simulate a CLI-based VFS environment.
- Practice memory, pointer, and buffer management in C.
- Gain OS-level insight into inode tables, file descriptors, and permissions.

---

## 👨‍💻 Author

**Mahesh Pawar**  
📫 Email: [mahesh.dinkar.pawar.02@gmail.com](mailto:mahesh.dinkar.pawar.02@gmail.com)  
📞 Phone: +91 9322150275  
🏢 Chikhali, Pune, Maharastra - 411062

---
