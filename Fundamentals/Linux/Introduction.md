# Linux Overview

## 🔹 First: Linux History — The Short Story

### 📌 1. The Beginning (1969 – UNIX)

Everything starts with **UNIX**, created in 1969 at Bell Labs. It followed the philosophy: *“Do one thing, and do it well.”*
Linux later inherited this spirit.

---

### 📌 2. Minix (1987)

Professor Andrew Tanenbaum created **Minix**, an educational UNIX‑like OS. Linus Torvalds used Minix as inspiration while learning systems programming.

---

### 📌 3. Birth of Linux (1991)

In 1991, **Linus Torvalds** began building his own kernel as a hobby project. Developers worldwide joined after his public announcement. This marked the start of the **Linux kernel** — open-source and community-driven.

---

### 📌 4. Distributions and Growth (1990s–Today)

The Linux ecosystem grew into many distributions:

* Debian
* Red Hat
* Ubuntu
* Fedora
* Kali
* Arch

Today, Linux powers servers, cloud platforms, supercomputers, and embedded devices.

---

## 🔹 Second: Linux Structure — How the System Is Built

Linux uses a clean, layered architecture:

### 1. Kernel (The Core)

The **kernel** manages hardware access, memory, CPU scheduling, networking, and devices.

### 2. System Libraries

Libraries like **glibc** provide high-level functions applications use to interact with the kernel.

### 3. System Tools

Essential command-line utilities such as `ls`, `cp`, `mv`, `ps`, and `cat` define the basic user environment.

### 4. User Space

Everything users interact with:

* Shells (Bash, Zsh)
* Desktop environments (GNOME, KDE)
* Applications (Firefox, VSCode)
* Server software (Nginx, MySQL)

---

# 🔹 Linux Components — Core Parts of the System

### 1. Kernel

The core that communicates with the hardware and manages low-level operations.

### 2. System Libraries

Provide interfaces for programs to interact with the kernel.

### 3. System Utilities

Basic tools for system management (`ls`, `rm`, `ps`, `kill`).

### 4. Shell

The command interpreter connecting users to the system.

### 5. User Applications

Browsers, editors, servers, and any user-level programs.

### 6. File System

Organizes files, permissions, and storage.

### 7. Hardware Layer

The CPU, RAM, storage, GPU, network interfaces, and devices the kernel interacts with.

---

# 📁 Linux File System Hierarchy — Explained

Linux uses a unified directory tree starting at `/`.

### /

Root of the entire filesystem.

### /bin

Essential user commands (`ls`, `cp`, `mv`).

### /sbin

System administration tools.

### /home

Home directories for users, e.g., `/home/kareem`.

### /root

Home directory for the root user.

### /usr

Major system resources:

* `/usr/bin` — user commands
* `/usr/sbin` — admin tools
* `/usr/lib` — libraries
* `/usr/share` — shared resources

### /etc

Configuration files.

### /var

Variable data (logs, caches, spools).

### /tmp

Temporary files.

### /boot

Bootloader files and the kernel.

### /dev

Device files (e.g., `/dev/sda`).

### /proc

Virtual system info (CPU, memory).

### /sys

Hardware and kernel interface.

### /opt

Optional third‑party software.

### /mnt & /media

Mount points for external storage.

---

# 🔥 Summary

* Everything starts from `/`.
* Linux is built from layers: **Kernel → Libraries → Tools → Shell → Applications → Filesystem → Hardware**.
* `/etc` = configs, `/var` = variable data, `/home` = user data, `/usr` = most applications.
