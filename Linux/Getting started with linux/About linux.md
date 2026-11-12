# Linux Commands in Action

## Introduction

Linux is an open-source operating system.

There are different Linux distributions available, including:

- Ubuntu
- CentOS
- Red Hat Enterprise Linux (RHEL)
- Alpine Linux
- Kali Linux

---

## Basic Linux Commands

### List Files and Directories

```bash
ls
```

Lists all files and directories in the current location.

### Create a Directory

```bash
mkdir <folder-name>
```

Example:

```bash
mkdir projects
```

### Create Multiple Directories

```bash
mkdir -p <folders>
```

Example:

```bash
mkdir -p Linux/{users,networking,storage}
```

### Print Working Directory

```bash
pwd
```

Displays the current directory path.

### Change Directory

```bash
cd <directory>
```

Example:

```bash
cd projects
```

### Move Back One Directory

```bash
cd ..
```

### Move Up and Enter Another Directory

```bash
cd ../<folder-name>
```

Example:

```bash
cd ../production
```

### Create an Empty File

```bash
touch <file-name>
```

Example:

```bash
touch notes.txt
```

### Print Text to Terminal

```bash
echo "Hello World"
```

### Append Text to a File

```bash
echo "This is an empty file" >> empty_file.txt
```

### Copy Files and Directories

```bash
cp <source> <destination>
```

Example:

```bash
cp file.txt backup/
```

---

# VI / VIM Editor

Vim primarily operates in two modes:

- **Normal Mode** (for navigation and editing commands)
- **Insert Mode** (for typing text)

To enter Insert Mode:

```text
i
```

To return to Normal Mode:

```text
Esc
```

---

## Navigation

| Key | Action |
|------|---------|
| h | Move left |
| j | Move down |
| k | Move up |
| l | Move right |
| Arrow Keys | Navigate around the file |

---

## Editing Commands

### Delete a Character

```text
x
```

### Delete Current Line

```text
dd
```

### Delete Multiple Lines

```text
3dd
```

Deletes the current line and the next two lines.

### Copy a Line

```text
yy
```

### Paste Copied Content

```text
p
```

---

## Scrolling

### Scroll Up

```text
Ctrl + U
```

### Scroll Down

```text
Ctrl + D
```

---

## Command Mode

Press:

```text
Esc
```

Then:

```text
:
```

to enter Command Mode.

### Quit

```text
:q
```

### Quit Without Saving

```text
:q!
```

### Save File

```text
:w
```

### Save and Quit

```text
:wq
```

or

```text
:x
```

---

## Quick Reference

| Command | Description |
|----------|------------|
| ls | List files and directories |
| mkdir | Create a directory |
| mkdir -p | Create multiple/parent directories |
| pwd | Show current directory |
| cd | Change directory |
| cd .. | Move to parent directory |
| touch | Create a file |
| echo | Print text |
| cp | Copy files/directories |
| yy | Copy a line in Vim |
| p | Paste in Vim |
| dd | Delete a line |
| 3dd | Delete 3 lines |
| :w | Save |
| :q | Quit |
| :q! | Quit without saving |
| :wq | Save and quit |

---

## Practice Lab

```bash
mkdir linux-practice
cd linux-practice

mkdir -p Linux/{users,permissions,networking}

touch notes.txt

echo "Linux commands practice" >> notes.txt

ls
pwd
```