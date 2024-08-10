## Table of Contents

1. [What is Linux?](#what-is-linux)
2. [Origin of Linux](#origin-of-linux)
3. [Linux Distributions](#linux-distributions)
4. [Linux File System](#linux-file-system)
5. [Linux Kernel](#linux-kernel)
6. [Linux Commands](#linux-commands)
7. [What is Bash Script?](#what-is-bash-script)
8. [Bash Script Exercises](#bash-script-exercises)
9. [Lab Tasks](#lab-tasks)


## What is Linux?
- **Definition**: Linux is an open-source operating system based on the Unix architecture. It is widely used in servers, desktops, and embedded systems.
- **Features**: Linux is known for its stability, security, and flexibility. It allows users to control the system at a granular level and supports a wide range of applications.

## Origin of Linux
- **Background**: Linux was created by Linus Torvalds in 1991. It began as a personal project to create a free and open-source alternative to the Unix operating system. Linus Torvalds, a Finnish software engineer, started working on the Linux kernel as a student at the University of Helsinki.
- **Initial Release**: The first version of Linux (0.01) was released in September 1991. It was a minimal kernel with basic features and limited hardware support.
- **Community Contribution**: Linux quickly gained traction within the open-source community, with many developers contributing to its growth and development. This collaborative approach led to rapid improvements and the expansion of Linux’s capabilities.
- **Growth**: Over the years, Linux has evolved into a powerful and versatile operating system used in a wide range of environments, from servers and desktops to mobile devices and embedded systems.

## Linux Distributions
- **Definition**: A Linux distribution (or distro) is a version of the Linux operating system that includes the Linux kernel and a selection of software packages tailored for specific use cases or user preferences.
- **Examples**: Some popular distributions include Ubuntu, Fedora, Debian, and CentOS. Each distribution may differ in its default software, package management system, and target audience.

## Linux File System

- **`/` (Root Directory)**: The top-level directory that contains all other directories.
- **`/bin`**: Contains essential command binaries (e.g., `ls`, `cp`, `mv`).
- **`/etc`**: Contains system configuration files.
- **`/home`**: Contains user directories. Each user has a subdirectory here (e.g., `/home/username`).
- **`/var`**: Contains variable data files like logs and spool files.
- **`/tmp`**: Contains temporary files created by applications.
- **`/usr`**: Contains user-related programs and data, including application binaries and libraries.

## Linux Kernel
- **Definition**: The kernel is the core component of the Linux operating system. It manages hardware resources, system calls, and facilitates communication between hardware and software.
- **Role**: The kernel handles tasks such as process management, memory management, and device drivers. It provides a bridge between applications and the physical hardware.


## Linux Commands
- **Purpose**: Commands are used to interact with the Linux system. They can perform a wide range of tasks, from file manipulation to system monitoring.
- **Examples**:
    - **`ls`**: Lists directory contents.
    - **`cd`**: Changes the current directory.
    - **`cp`**: Copies files and directories.
    - **`rm`**: Removes files or directories.
    - **`ps`**: Displays information about running processes.


## What is Bash Script?
- **Definition**: Bash (Bourne Again SHell) is a command-line interpreter and scripting language for Unix-like operating systems. A Bash script is a file containing a series of commands written in the Bash language.
- **Purpose**: Bash scripts automate repetitive tasks, such as file manipulation, program execution, and system administration. They allow users to create complex workflows and manage system operations efficiently.
- Basic Example:
    ```bash
    #!/bin/bash
    echo "Hello, World!"
    ```
    - **`#!/bin/bash`**: Shebang line indicating the script should be run using Bash.
    - **`echo "Hello, World!"`**: A command that prints "Hello, World!" to the terminal.


## Bash Script Exercises
1. Write a script to create folders: LAB2 to LAB12.
2. Modify the script above to rename folders: LAB02 to LAB012.
3. Write the script convert the uppercase to lowercase and rename the folders Lab02 to lab012.
4. Write a script to delete all the swp files in your system or directory.
5. Modify the script above to delete the input file name in your system or directory. 

### Answers
1. Write a script to create folders: LAB2 to LAB12
    ```bash
    #!/bin/bash
   
    for i in {2..12}
    do
    mkdir "LAB$i"
    done
    ```

2. Modify the Script to Rename Folders from LAB02 to LAB012
    ```bash
    #!/bin/bash
   
    for i in {2..12}
    do
    mkdir "LAB$(printf "%02d" $i)"
    done
    ```
   
3. Script to Convert Uppercase to Lowercase and Rename Folders

    ```bash
    #!/bin/bash

    for dir in LAB*
    do
    if [ -d "$dir" ]; then
    new_dir=$(echo "$dir" | tr '[:upper:]' '[:lower:]')
    mv "$dir" "$new_dir"
    fi
    done
    ```
   
4. Script to Delete All .swp Files in Your System or Directory
    ```bash
    #!/bin/bash

    find / -type f -name "*.swp" -delete
    ```
   
5. Modify the Script to Delete a Specific Input File
    ```bash
    #!/bin/bash

    echo "Enter the filename to delete:"
    read filename
    
    if [ -f "$filename" ]; then
    rm "$filename"
    echo "$filename deleted."
    else
    echo "$filename does not exist."
    fi
    ```
   
## Lab Tasks
1. Write a Shell Script to output a specified directory's size.
2. Write a Shell Bash Script to evaluate the status of a file/directory.
3. Write a Shell Bash Script to report server related information.
4. Write a Shell Bash Script to report if CPU usage exceeds the threshold.
5. Write a Shell Bash Script to check if the disk space crosses the limit.
6. Write a Shell Bash Script to gather information related to the server.
7. Write a Shell Bash Script to back up a local file into a remote server.
8. Write a Shell Bash Script to show hardware information for systems Linux.
9. Write a Shell Bash Script to show CPU temperature.
10. Write a Shell Bash Script to check if a number input from standard input is odd or even.
11. Write a Shell Bash Script to check if a provided number is Armstrong or not.
12. Write a Shell Bash Script to check if a number is prime or not.
13. Write a Shell Bash Script to convert Decimal Numbers to Binary.
14. Write a Shell Bash Script to Get the location of an IP address.
15. Write a Shell Bash Script to archive a path into a file and encrypt the file.

### Answers
1. Script to Output a Specified Directory's Size
    ```bash
    #!/bin/bash

    echo "Enter the directory path:"
    read dir_path
    
    if [ -d "$dir_path" ]; then
    du -sh "$dir_path"
    else
    echo "Directory does not exist."
    fi
    ```
   
2. Script to Evaluate the Status of a File/Directory
    ```bash
    #!/bin/bash

    echo "Enter the file or directory path:"
    read path
    
    if [ -e "$path" ]; then
    if [ -d "$path" ]; then
    echo "$path is a directory."
    elif [ -f "$path" ]; then
    echo "$path is a file."
    else
    echo "$path is a special file."
    fi
    else
    echo "$path does not exist."
    fi
    ```
   
3. Script to Report Server-Related Information
    ```bash
   #!/bin/bash

    echo "Server Information:"
    echo "Hostname: $(hostname)"
    echo "OS Version: $(uname -a)"
    echo "Uptime: $(uptime -p)"
    echo "IP Addresses: $(hostname -I)"
    echo "Disk Usage:"
    df -h
    echo "Memory Usage:"
    free -h
    ```
   
4. Script to Report if CPU Usage Exceeds a Threshold
    ```bash
    #!/bin/bash

    THRESHOLD=80
    CPU_USAGE=$(top -bn1 | grep "Cpu(s)" | sed "s/.*, *\([0-9.]*\)%* id.*/\1/" | awk '{print 100 - $1}')
    
    if (( $(echo "$CPU_USAGE > $THRESHOLD" | bc -l) )); then
    echo "CPU usage is above threshold: $CPU_USAGE%"
    else
    echo "CPU usage is below threshold: $CPU_USAGE%"
    fi
    ```
   
5. Script to Check if Disk Space Crosses a Limit
    ```bash
    #!/bin/bash

    THRESHOLD=80
    DISK_USAGE=$(df / | grep / | awk '{ print $5 }' | sed 's/%//g')
    
    if [ "$DISK_USAGE" -gt "$THRESHOLD" ]; then
    echo "Disk space usage is above threshold: $DISK_USAGE%"
    else
    echo "Disk space usage is below threshold: $DISK_USAGE%"
    fi
    ```
   
6. Script to Gather Information Related to the Server
    ```bash
    #!/bin/bash

    #!/bin/bash

    echo "Gathering server information..."
    echo "Hostname: $(hostname)"
    echo "OS Version: $(uname -a)"
    echo "Uptime: $(uptime -p)"
    echo "IP Addresses: $(hostname -I)"
    echo "Disk Usage:"
    df -h
    echo "Memory Usage:"
    free -h
    echo "CPU Usage:"
    top -bn1 | grep "Cpu(s)"
    ```
   
7. Script to back up a Local File to a Remote Server
    ```bash
    #!/bin/bash

    echo "Enter the local file path:"
    read local_file
    echo "Enter the remote server user@host:path:"
    read remote_path
    
    if [ -f "$local_file" ]; then
    scp "$local_file" "$remote_path"
    echo "Backup completed."
    else
    echo "Local file does not exist."
    fi
    ```

8. Script to Show Hardware Information for Linux Systems
    ```bash
   #!/bin/bash

    echo "Hardware Information:"
    echo "CPU Info:"
    lscpu
    echo "Memory Info:"
    lsmem
    echo "Disk Info:"
    lsblk
    echo "PCI Devices:"
    lspci
    ```
   
9. Script to Show CPU Temperature
    ```bash
   #!/bin/bash

    if command -v sensors >/dev/null 2>&1; then
    echo "CPU Temperature:"
    sensors | grep 'Core 0'
    else
    echo "sensors command not found. Install lm-sensors package."
    fi
   ```

10. Script to Check if a Number Input is Odd or Even
    ```bash
    #!/bin/bash

    echo "Enter a number:"
    read number
    
    if (( number % 2 == 0 )); then
    echo "$number is even."
    else
    echo "$number is odd."
    fi
    ```

11. Script to Check if a Number is Armstrong or Not
    ```bash
    #!/bin/bash

    echo "Enter a number:"
    read number
    
    num_len=${#number}
    sum=0
    temp=$number
    
    while [ $temp -gt 0 ]
    do
    digit=$((temp % 10))
    sum=$((sum + digit**num_len))
    temp=$((temp / 10))
    done
    
    if [ $sum -eq $number ]; then
    echo "$number is an Armstrong number."
    else
    echo "$number is not an Armstrong number."
    fi
    ```
    
12. Script to Check if a Number is Prime or Not
    ```bash
    #!/bin/bash

    echo "Enter a number:"
    read number
    
    if [ "$number" -lt 2 ]; then
    echo "$number is not a prime number."
    exit
    fi
    
    for ((i = 2; i <= number / 2; i++)); do
    if [ $((number % i)) -eq 0 ]; then
    echo "$number is not a prime number."
    exit
    fi
    done
    
    echo "$number is a prime number."
    ```
    
13. Script to Convert Decimal Numbers to Binary
    ```bash
    #!/bin/bash

    echo "Enter a decimal number:"
    read decimal
    
    binary=$(echo "obase=2;$decimal" | bc)
    echo "Binary representation: $binary"
    ```

14. Script to Get the Location of an IP Address
    ```bash
    #!/bin/bash

    echo "Enter an IP address:"
    read ip_address
    
    if command -v curl >/dev/null 2>&1; then
    curl -s "http://ipinfo.io/$ip_address"
    else
    echo "curl command not found."
    fi
    ```
    
15. Script to Archive a Path into a File and Encrypt the File
    ```bash
    #!/bin/bash

    echo "Enter the directory or file path to archive:"
    read path
    echo "Enter the archive file name (e.g., archive.tar.gz):"
    read archive_name
    echo "Enter the encryption password:"
    read -s password
    
    tar -czf "$archive_name" "$path"
    openssl enc -aes-256-cbc -salt -in "$archive_name" -out "$archive_name.enc" -pass pass:"$password"
    rm "$archive_name"
    echo "Archive created and encrypted."
    ```