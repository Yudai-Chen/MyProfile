---
title: Yalnix Operating System
summary: A Unix-like Operating System for RCS421 simulated hardware and X11 Windows System.
date: "2020-05-20T00:00:00Z"
external_link: ""

image:
  caption: Yudai Chen
  focal_point: Smart
  
slides: example
---
+ Yalnix OS is a Unix-like Operating System for RCS421 simulated hardware and X11 Windows System, including both kernel and file system with all basic functionalities such as memory management, interrupt handling, context switching and I/O handling.

+ Achieved a process scheduler based on Round-Robin algorithm to support multiple processes with content switch and kernel/user mode protection, supporting multiple C programs loaded-in and executed concurrently.

+ Implemented memory management using virtual memory and single-level page table (as well as TLB), supporting both static and dynamic memory allocation in user processes.

+ Implemented system calls including Fork, Wait, Exec, Sleep, Brk, Open/Close, Read/Write, Link, MkDir, ChDir, TtyRead, etc.

+ Created a terminal device driver, supporting keyboard input, multiple virtual monitors and multiple processes access.

+ Built a file system based on demand paging with an LRU cache, supporting multiple users running on top of the Yalnix kernel, supporting large file storage using indirect inodes.