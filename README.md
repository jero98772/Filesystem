# FileSystem

![](https://raw.githubusercontent.com/jero98772/Filesystem/refs/heads/main/docs/1.png)

FileSystem is a toy, educational filesystem written in Python that simulates how a real operating system manages files at multiple abstraction levels. It runs on top of a virtual disk image and exposes an interactive shell for exploring filesystem behavior in a safe, inspectable way.

### Install

	git clone https://github.com/jero98772/Filesystem.git

	pip install -r requieriements.txt

	python main.py



The system is structured into four clear layers, each mirroring a real OS filesystem stack:

Block Device Layer
The lowest level, responsible for reading and writing fixed-size blocks to a disk image file. This layer abstracts raw storage and allows direct inspection of bytes, making it ideal for understanding how data is physically laid out.

Block Allocation Layer
Manages free and used blocks using allocation strategies similar to real filesystems. It decides where files and directories are stored on disk and tracks space usage.

Inode & Metadata Layer
Represents files and directories using inodes, storing metadata such as file type, size, timestamps, and block pointers. This layer bridges raw storage with logical filesystem structures.

Directory & Shell Layer
The highest layer, providing a Unix-like interface (ls, cd, cat, mkdir, rm, write, etc.) and a directory tree view. This layer translates user commands into filesystem operations.

By separating responsibilities across these layers, the project demonstrates key operating system concepts such as persistence, abstraction, metadata management, and filesystem traversal—making it well-suited for learning, experimentation, and teaching.
