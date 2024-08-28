
# Linux Command Cheatsheet

## File System Operations

- **`ls`**: List directory contents.
  - **Example**: 
    ```bash
    ls -l
    ```
    *(Displays a detailed list of files with permissions.)*

- **`cd`**: Change the current directory.
  - **Example**: 
    ```bash
    cd /home/user/Documents
    ```
    *(Navigates to the Documents directory.)*

- **`pwd`**: Print the current working directory.
  - **Example**: 
    ```bash
    pwd
    ```
    *(Shows the full path of the current directory.)*

- **`mkdir`**: Create a new directory.
  - **Example**: 
    ```bash
    mkdir my_folder
    ```
    *(Creates a directory named `my_folder`.)*

- **`cp`**: Copy files or directories.
  - **Example**: 
    ```bash
    cp file.txt /backup/
    ```
    *(Copies `file.txt` to the `/backup/` directory.)*

- **`mv`**: Move or rename files and directories.
  - **Example**: 
    ```bash
    mv old_name.txt new_name.txt
    ```
    *(Renames `old_name.txt` to `new_name.txt`.)*

- **`rm`**: Remove files or directories.
  - **Example**: 
    ```bash
    rm -r my_folder
    ```
    *(Recursively deletes `my_folder` and its contents.)*

- **`touch`**: Create an empty file.
  - **Example**: 
    ```bash
    touch newfile.txt
    ```
    *(Creates an empty file named `newfile.txt`.)*

- **`cat`**: View the contents of a file.
  - **Example**: 
    ```bash
    cat file.txt
    ```
    *(Displays the contents of `file.txt`.)*

- **`nano`**: Simple text editor for creating and editing files.
  - **Example**: 
    ```bash
    nano file.txt
    ```
    *(Opens `file.txt` for editing in the Nano text editor.)*

---

## File Permissions

- **`chmod`**: Change file access permissions.
  - **Example**: 
    ```bash
    chmod 755 script.sh
    ```
    *(Sets permissions to read, write, and execute for the owner, and read and execute for others.)*

- **`chown`**: Change file ownership.
  - **Example**: 
    ```bash
    chown user:group file.txt
    ```
    *(Changes the owner of `file.txt` to `user` and the group to `group`.)*

- **`chgrp`**: Change the group ownership of a file.
  - **Example**: 
    ```bash
    chgrp developers file.txt
    ```
    *(Changes the group of `file.txt` to `developers`.)*

---

## Process Management

- **`ps`**: Display information about active processes.
  - **Example**: 
    ```bash
    ps aux
    ```
    *(Shows detailed information about all running processes.)*

- **`top`**: Display a dynamic, real-time list of processes.
  - **Example**: 
    ```bash
    top
    ```
    *(Continuously displays system processes, CPU, and memory usage.)*

- **`htop`**: Interactive process viewer (requires installation).
  - **Example**: 
    ```bash
    htop
    ```
    *(Provides an interactive, color-coded view of system processes.)*

- **`kill`**: Terminate a process using its PID.
  - **Example**: 
    ```bash
    kill 1234
    ```
    *(Terminates the process with PID 1234.)*

- **`killall`**: Terminate all processes by name.
  - **Example**: 
    ```bash
    killall firefox
    ```
    *(Kills all running instances of Firefox.)*

---

## System Information

- **`uname`**: Display system information.
  - **Example**: 
    ```bash
    uname -a
    ```
    *(Shows detailed information about the system, including kernel version.)*

- **`df`**: Report file system disk space usage.
  - **Example**: 
    ```bash
    df -h
    ```
    *(Displays disk space usage in a human-readable format.)*

- **`free`**: Show memory usage statistics.
  - **Example**: 
    ```bash
    free -m
    ```
    *(Displays memory usage in megabytes.)*

- **`hostname`**: Display or set the system's hostname.
  - **Example**: 
    ```bash
    hostname
    ```
    *(Shows the current hostname of the system.)*

---

## Networking

- **`ifconfig`**: Configure network interfaces (deprecated, use `ip` instead).
  - **Example**: 
    ```bash
    ifconfig eth0
    ```
    *(Displays configuration for the `eth0` interface.)*

- **`ping`**: Check network connectivity by sending packets.
  - **Example**: 
    ```bash
    ping google.com
    ```
    *(Sends ICMP echo requests to `google.com`.)*

- **`netstat`**: Display network connections, routing tables, etc.
  - **Example**: 
    ```bash
    netstat -tuln
    ```
    *(Shows listening ports and their status.)*

- **`iptables`**: Configure packet filtering rules (requires root privileges).
  - **Example**: 
    ```bash
    iptables -L
    ```
    *(Lists all current firewall rules.)*

---

## Package Management

- **`apt-get`**: Manage packages on Debian-based systems.
  - **Example**: 
    ```bash
    sudo apt-get install vim
    ```
    *(Installs the `vim` text editor.)*

- **`yum`**: Package manager for RPM-based distributions.
  - **Example**: 
    ```bash
    sudo yum install httpd
    ```
    *(Installs the Apache HTTP Server.)*

- **`rpm`**: Manage RPM packages.
  - **Example**: 
    ```bash
    rpm -ivh package.rpm
    ```
    *(Installs an RPM package with verbose output and progress bar.)*

---

## Shell Scripting

- **`bash`**: GNU Bourne-Again SHell, widely used command interpreter.
  - **Example**: 
    ```bash
    bash script.sh
    ```
    *(Runs a shell script named `script.sh`.)*

- **`sh`**: Bourne shell, a simple command interpreter.
  - **Example**: 
    ```bash
    sh script.sh
    ```
    *(Executes `script.sh` using the Bourne shell.)*

- **`awk`**: A pattern scanning and processing language.
  - **Example**: 
    ```bash
    awk '{print $1}' file.txt
    ```
    *(Prints the first column from `file.txt`.)*

- **`sed`**: Stream editor for filtering and transforming text.
  - **Example**: 
    ```bash
    sed 's/old/new/g' file.txt
    ```
    *(Replaces all occurrences of "old" with "new" in `file.txt`.)*

---

## File Transfer

- **`scp`**: Securely copy files between hosts.
  - **Example**: 
    ```bash
    scp file.txt user@remote:/path/
    ```
    *(Copies `file.txt` to a remote server.)*

- **`rsync`**: Efficiently sync files between locations.
  - **Example**: 
    ```bash
    rsync -avz /src/ /dst/
    ```
    *(Synchronizes the contents of `/src/` to `/dst/` with archive mode and compression.)*

---

## User and Group Management

- **`useradd`**: Create a new user account.
  - **Example**: 
    ```bash
    sudo useradd newuser
    ```
    *(Creates a new user named `newuser`.)*

- **`userdel`**: Remove a user account.
  - **Example**: 
    ```bash
    sudo userdel newuser
    ```
    *(Deletes the user `newuser`.)*

- **`usermod`**: Modify a user account's details.
  - **Example**: 
    ```bash
    sudo usermod -aG sudo newuser
    ```
    *(Adds `newuser` to the `sudo` group.)*

- **`groupadd`**: Create a new group.
  - **Example**: 
    ```bash
    sudo groupadd developers
    ```
    *(Creates a new group called `developers`.)*

- **`groupdel`**: Delete a group.
  - **Example**: 
    ```bash
    sudo groupdel developers
    ```
    *(Deletes the `developers` group.)*

- **`groupmod`**: Modify group properties.
  - **Example**: 
    ```bash
    sudo groupmod -n newgroup developers
    ```
    *(Renames the `developers` group to `newgroup`.)*

---

## System Services

- **`systemctl`**: Manage systemd services and units.
  - **Example**: 
    ```bash
    sudo systemctl restart nginx
    ```
    *(Restarts the Nginx service.)*

- **`service`**: Control services (used in SysVinit systems).
  - **Example**: 
    ```bash
    sudo service apache2 start
    ```
    *(Starts the Apache service.)*

- **`chkconfig`**: Configure services to start at boot (used in SysVinit systems).
  - **Example**: 
    ```bash
    sudo chkconfig httpd on
    ```
    *(Enables the `httpd` service to start at boot.)*

---
