# Born2beRoot - System Administration Project

## Project Overview

**Born2beRoot** is a system administration project that introduces the fundamental concepts of virtualization and server configuration. Through this project, I learned how to set up and secure a virtual server while adhering to strict system rules and policies. The project involved using VirtualBox (or UTM) to install and configure a Linux-based operating system (Debian or Rocky), focusing on implementing critical security measures such as encryption, firewall configuration, and password policies.

---

## Key Features

### 1. Virtual Machine Setup

- **Operating System**: Either the latest stable version of Debian or Rocky Linux.
- **Virtualization Tool**: VirtualBox (or UTM as an alternative).
- **LVM Partitioning**: Created and encrypted at least two partitions using LVM (Logical Volume Manager).

### 2. Server Configuration

- **SSH Setup**: Configured SSH to run on port 4242, with root login disabled for security.
- **Firewall Configuration**: Used UFW (or firewalld for Rocky) to secure the virtual machine, leaving only port 4242 open.
- **Hostname**: Set the hostname to include my 42 login, ensuring the machine's identification.
- **User Management**: Configured a user with my login, added to the `user42` and `sudo` groups.

### 3. Security Policies

- **Password Policy**: 
  - Passwords expire every 30 days.
  - Minimum password length of 10 characters, including an uppercase letter, a lowercase letter, and a number.
  - Passwords must not contain the username or more than three consecutive identical characters.
  - Warnings are issued 7 days before password expiration.
  
- **Sudo Configuration**:
  - Limited to 3 incorrect password attempts.
  - Displayed a custom error message on wrong password attempts.
  - Archived all sudo command logs.
  - Enabled TTY mode and restricted sudo paths.

### 4. Monitoring Script

Developed a bash script (`monitoring.sh`) that periodically displays critical system information every 10 minutes, including:

- System architecture and kernel version
- Number of physical and virtual processors
- RAM and storage utilization
- CPU usage
- Last reboot date and time
- Active LVM status
- Number of active connections and users
- IP address and MAC address
- Number of commands executed with sudo

---

## Skills Demonstrated

- **System Virtualization**: Successfully deployed and configured a virtual machine using VirtualBox (or UTM).
- **Server Security**: Applied strict security measures, including password policies and SSH hardening.
- **Firewall Management**: Configured UFW/firewalld to control network access.
- **Linux Administration**: Gained experience with command-line tools and managing services without a graphical interface.
- **Automation with Bash**: Developed a monitoring script to automate the display of server statistics.

---

## Conclusion

The **Born2beRoot** project provided hands-on experience in setting up and securing a server in a virtualized environment. It emphasized the importance of strong security policies, effective user management, and system monitoring. These skills are essential for maintaining reliable and secure server environments in real-world scenarios.
