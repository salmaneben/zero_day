# 0x00. Vagrant - Introduction to Virtual Machines

![Vagrant](https://img.shields.io/badge/Vagrant-2.2.6+-blue)
![Ubuntu](https://img.shields.io/badge/Ubuntu-20.04%20LTS-orange)
![VirtualBox](https://img.shields.io/badge/VirtualBox-6.1+-green)

## 📋 Project Description

This project introduces the fundamentals of virtualization and development environment management using Vagrant. You'll learn how to create, configure, and manage virtual machines for consistent development environments across different systems.

## 🎯 Learning Objectives

At the end of this project, you should be able to explain:

- **What is a virtual machine?**
  - A software-based computer that runs inside another computer
  - Provides isolated environment for testing and development
  - Enables running different operating systems on the same hardware

- **What is Vagrant?**
  - A tool for building and managing virtual machine environments
  - Provides easy configuration and reproducible environments
  - Uses simple configuration files (Vagrantfile)

- **Who wrote Vagrant?**
  - Created by Mitchell Hashimoto
  - Developed by HashiCorp

- **What is Ubuntu?**
  - Popular Linux distribution based on Debian
  - Known for user-friendliness and strong community support
  - Widely used in server and development environments

- **What does "Ubuntu" mean?**
  - African philosophy meaning "humanity to others"
  - "I am because we are" - emphasizing interconnectedness

- **How to use VMs with Vagrant**
  - Initialize, configure, and manage virtual machines
  - Use `vagrant up`, `vagrant ssh`, `vagrant halt` commands
  - Share files between host and guest systems

- **What does the command `uname` do?**
  - Displays system information
  - Shows kernel name, version, and system architecture

## 🛠️ Environment Setup

### Prerequisites

Ensure you have the following installed on your system:

1. **Vagrant** (version 2.2.6 or higher)
   ```bash
   # Download from: https://www.vagrantup.com/downloads
   vagrant --version
   ```

2. **VirtualBox** (version 6.1 or higher)
   ```bash
   # Download from: https://www.virtualbox.org/wiki/Downloads
   VBoxManage --version
   ```

### Initial Setup

1. **Create project directory:**
   ```bash
   mkdir vagrant_project
   cd vagrant_project
   ```

2. **Initialize Vagrant:**
   ```bash
   vagrant init ubuntu/focal64
   ```

3. **Start the virtual machine:**
   ```bash
   vagrant up
   ```

4. **Connect to the VM:**
   ```bash
   vagrant ssh
   ```

## 📁 Files in This Project

| File | Description |
|------|-------------|
| `README.md` | This documentation file |
| `0-hello_ubuntu` | Script that prints the kernel name using `uname` |

## 📝 Tasks

### 0. Hello Ubuntu (mandatory)

**Objective:** Inside the Ubuntu virtual machine, create a script that prints the kernel name.

**File:** `0-hello_ubuntu`

**Requirements:**
- The script should print the result of `uname` command
- Must be exactly one line
- Should output: `Linux`

**Solution:**
```bash
#!/bin/bash
uname
```

**How to test:**
```bash
vagrant ssh
cd /vagrant
cat 0-hello_ubuntu
./0-hello_ubuntu
```

**Expected output:**
```
Linux
```

## 🔧 Common Vagrant Commands

| Command | Description |
|---------|-------------|
| `vagrant init [box]` | Initialize a new Vagrant environment |
| `vagrant up` | Start and provision the Vagrant environment |
| `vagrant ssh` | SSH into the running Vagrant machine |
| `vagrant halt` | Shut down the running machine |
| `vagrant reload` | Restart the machine and reload configuration |
| `vagrant destroy` | Stop and delete all traces of the machine |
| `vagrant status` | Show the status of the machines |
| `vagrant suspend` | Suspend the machine |
| `vagrant resume` | Resume a suspended machine |

## 🐛 Troubleshooting

### Common Issues and Solutions

1. **Vagrant command not found:**
   - Ensure Vagrant is properly installed and in your PATH
   - Restart your terminal after installation

2. **VirtualBox not found:**
   - Install VirtualBox before using Vagrant
   - Check that virtualization is enabled in BIOS

3. **VM fails to start:**
   - Check if Hyper-V is disabled (Windows)
   - Ensure sufficient RAM and disk space
   - Try different box versions

4. **SSH connection issues:**
   - Use `vagrant reload` to restart the machine
   - Check VM status with `vagrant status`

## 📊 System Information Commands

Learn these essential Linux commands for system information:

```bash
# Display kernel information
uname -a                    # All system information
uname -s                    # Kernel name (Linux)
uname -r                    # Kernel release
uname -m                    # Machine architecture

# Display system information
hostnamectl                 # System hostname and info
lsb_release -a             # Distribution information
cat /etc/os-release        # OS release information

# Display hardware information
lscpu                      # CPU information
free -h                    # Memory usage
df -h                      # Disk space usage
```

## 🎓 Additional Learning Resources

- [Vagrant Documentation](https://www.vagrantup.com/docs)
- [Ubuntu Server Guide](https://ubuntu.com/server/docs)
- [VirtualBox Manual](https://www.virtualbox.org/manual/)
- [Linux Command Line Basics](https://ubuntu.com/tutorials/command-line-for-beginners)

## ✅ Requirements

### General
- All files will be interpreted on Ubuntu 20.04 LTS
- All files should end with a new line
- A `README.md` file at the root of the folder is mandatory
- All scripts must be executable

### Vagrant Specific
- Must use Vagrant version 2.2.6 or higher
- Virtual machine must be Ubuntu 20.04 LTS
- All commands must work in the Vagrant environment

## 🎯 Project Completion Checklist

- [ ] Vagrant and VirtualBox installed
- [ ] Virtual machine successfully created and running
- [ ] Can SSH into the VM
- [ ] `0-hello_ubuntu` script created and working
- [ ] Script outputs "Linux" when executed
- [ ] All files properly committed to Git

## 👨‍💻 Author

**Salman Ben**
- GitHub: [@salmaneben](https://github.com/salmaneben)

---

*This project is part of the ALX Software Engineering Program - DevOps Fundamentals*
