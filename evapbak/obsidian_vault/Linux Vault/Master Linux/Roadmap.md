# Phase 1 – Foundations (You Either Know This or You’re Faking It)
---


### 1. Terminal & Shell Mastery
Master:

- bash/zsh fundamentals
    
- pipes, redirection, subshells
    
- job control
    
- environment variables
    
- exit codes
    

Tools you must be fluent in:

- `grep`, `sed`, `awk`
    
- `cut`, `sort`, `uniq`
    
- `xargs`
    
- `find`
    
- `tar`, `rsync`
    
- `tmux`
    

If you cannot manipulate text streams like a weapon, you’re not advanced.

Read:

- The Linux Command Line
    
- Advanced Bash-Scripting Guide
    

---

### 2. Filesystem & Core Concepts

Understand:

- FHS (Filesystem Hierarchy Standard)
    
- inodes
    
- hard vs soft links
    
- permissions (chmod is basic — understand setuid, setgid, sticky bit)
    
- ACLs
    
- mounts
    
- block devices
    
- `/proc` and `/sys`
    

If you don’t understand how `/dev` works, you’re still surface-level.

---

### 3. Processes & System Control

Master:

- `ps`, `top`, `htop`
    
- signals
    
- `kill`, `pkill`
    
- process states
    
- cgroups basics
    

Understand:

- how PID 1 works
    
- what init systems do
    

Deep dive into:

- systemd  
    Learn:
    
    - units
        
    - targets
        
    - services
        
    - journald
        
    - timers
        

If systemd scares you, that’s a skill gap.

---

# Phase 2 – Real System Understanding

### 4. Boot Process

You must understand:

BIOS/UEFI → Bootloader → Kernel → Init → Userspace

Study:

- GRUB
    
- Linux kernel parameters
    
- initramfs
    

Rebuild your bootloader manually once. Break it. Fix it.

---

### 5. Package Management (Deep Level)

Not “I can install packages.”

Understand:

- dependency resolution
    
- shared libraries
    
- dynamic linking
    
- ld.so
    
- how `/usr/lib` works
    

Use:

- `ldd`
    
- `strace`
    
- `lsof`
    

Since you like Nix:

- Learn Nix derivations.
    
- Understand purity.
    
- Read the Nix source code for a small package.
    
- Debug a broken derivation manually.
    

---

### 6. Networking (Serious Level)

You’re not advanced until you understand networking.

Master:

- TCP/IP
    
- ports
    
- sockets
    
- DNS
    
- routing tables
    
- firewalls
    

Tools:

- `ip`
    
- `ss`
    
- `netstat`
    
- `tcpdump`
    
- `nmap`
    

Understand:

- nftables / iptables
    
- SSH internals
    

If you can’t explain what happens when you type `google.com` in a browser, you’re not there yet.

---

# Phase 3 – Kernel & Low-Level

Now it gets serious.

### 7. Kernel Knowledge

Study:

- monolithic vs modular kernel
    
- kernel modules
    
- syscalls
    
- virtual memory
    
- scheduling
    

Read parts of:

- Linux Kernel Development
    

Compile your own kernel.  
Remove features. Break hardware support. Fix it.

---

### 8. Filesystems Deep Dive

Understand:

- ext4 internals
    
- journaling
    
- btrfs
    
- xfs
    

Break a filesystem in a VM and recover it.

---

### 9. Memory & Performance

Learn:

- virtual memory
    
- swap
    
- overcommit
    
- OOM killer
    
- perf
    
- profiling tools
    

Use:

- `perf`
    
- `vmstat`
    
- `iostat`
    
- `free`
    
- `dmesg`
    

---

# Phase 4 – Programming + Internals

Linux mastery without programming = fraud.

You must know:

### 1. C

Not tutorials. Real C.

Understand:

- pointers deeply
    
- memory management
    
- syscalls
    
- POSIX
    

Read:

- The C Programming Language
    

Write:

- a mini shell
    
- a process manager
    
- a simple HTTP server
    

---

### 2. Read Source Code

Read:

- coreutils
    
- bash
    
- systemd components
    
- parts of the Linux kernel
    

Even if you understand 30%, that’s growth.

---

# Phase 5 – Build From Scratch

This is where 99% quit.

### Option A:

Install:

- Arch Linux  
    Manually configure everything.
    

### Option B (Hard Mode):

Follow:

- Linux From Scratch
    

Build a system completely from source.

If you complete LFS and understand it, you're beyond casual power user.

---

# Phase 6 – Real Mastery

Now we separate hobbyists from operators.

### 1. Security

- AppArmor / SELinux
    
- file capabilities
    
- namespaces
    
- containers (understand them, don’t just use Docker blindly)
    

### 2. Containers & Virtualization

Understand:

- namespaces
    
- cgroups
    
- KVM
    
- QEMU
    

### 3. Automation

- Ansible
    
- declarative infrastructure
    
- reproducible builds
    

Since you love efficiency — automate your entire system bootstrap.

---

# Phase 7 – Proof of Mastery

If you want to test yourself:

You should be able to:

- Recover a broken bootloader.
    
- Fix networking without internet.
    
- Debug why a service fails from logs only.
    
- Reduce system to minimal bootable state.
    
- Explain what happens from power button to shell prompt.
    
- Navigate entire system without mouse (you already enjoy this).
    

If you cannot do these under pressure, you’re not master level.

---

# Brutal Reality

Mastery is not:

- Fancy rice
    
- Hardest distro badge
    
- Reddit bragging
    
- Saying “I use NixOS btw”
    

Mastery is:

- Debugging at 3AM calmly
    
- Understanding before touching
    
- Reading source code without fear
    
- Staying on one system long enough to truly understand it


##### 19.02.2026 @nightkatt  





