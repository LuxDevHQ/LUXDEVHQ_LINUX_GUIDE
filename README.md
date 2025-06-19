# Top 50 Linux Commands You Must Know (Detailed Guide)

## File & Directory Management

### `ls` (List)
Lists directory contents.

- `ls`: Lists files and directories in the current directory
- `ls -l`: Lists in long format (permissions, owner, size, etc.)
- `ls -a`: Shows hidden files (starting with '.')
- `ls -lh`: Lists in human-readable format (e.g., KB, MB, GB)

**Example:** `ls -l /home/user/documents`

### `pwd` (Print Working Directory)
Displays the current directory path.

- `pwd`: Prints the absolute path of the current directory

### `cd` (Change Directory)
Navigates through directories.

- `cd <directory_path>`: Changes to the specified directory
- `cd ..`: Goes up one directory
- `cd`: Returns to the home directory

**Example:** `cd /var/log`

### `mkdir` (Make Directory)
Creates new directories.

- `mkdir <directory_name>`: Creates a new directory
- `mkdir -p <directory_path>`: Creates parent directories if needed

**Example:** `mkdir new_folder`

### `mv` (Move/Rename)
Moves or renames files and directories.

- `mv <source> <destination>`: Moves or renames the source to the destination

**Examples:**
- `mv old_file.txt new_file.txt` (renames)
- `mv file.txt /tmp` (moves)

### `cp` (Copy)
Copies files and directories.

- `cp <source> <destination>`: Copies the source to the destination
- `cp -r <source_directory> <destination_directory>`: Copies a directory recursively

**Example:** `cp file.txt file_copy.txt`

### `rm` (Remove)
Deletes files and directories.

- `rm <file>`: Deletes a file
- `rm -r <directory>`: Deletes a directory and its contents recursively (use with caution!)
- `rm -i <file>`: Prompts before deletion

**Example:** `rm unwanted_file.txt`

### `touch`
Creates empty files or updates file timestamps.

- `touch <file_name>`: Creates an empty file or updates its modification time

### `ln` (Link)
Creates symbolic (soft) or hard links.

- `ln -s <source> <link_name>`: Creates a symbolic link
- `ln <source> <link_name>`: Creates a hard link

### `clear`
Clears the terminal screen.

## Viewing & Editing Files

### `cat` (Concatenate)
Displays file contents.

- `cat <file>`: Displays the contents of a file

### `echo`
Prints text to the terminal.

- `echo "<text>"`: Prints the specified text

### `less`
Views file contents one page at a time.

- `less <file>`: Opens the file in a scrollable viewer
- Use spacebar to move forward, 'q' to quit

### `man` (Manual)
Displays command documentation.

- `man <command>`: Shows the manual page for the specified command

## System Information

### `uname` (Unix Name)
Displays system information.

- `uname -a`: Displays all system information
- `uname -s`: Kernel name
- `uname -n`: Hostname
- `uname -r`: Kernel release
- `uname -v`: Kernel version
- `uname -m`: Machine hardware name

### `whoami`
Displays the current username.

## Archives & Compression

### `tar` (Tape Archive)
Creates and extracts archives (often used for compression).

- `tar -cvf <archive_name>.tar <files>`: Creates a tar archive
- `tar -xvf <archive_name>.tar`: Extracts a tar archive
- `tar -czvf <archive_name>.tar.gz <files>`: Creates a gzipped tar archive
- `tar -xzvf <archive_name>.tar.gz`: Extracts a gzipped tar archive

### `zip`
Compresses files into a zip archive.

- `zip <archive_name>.zip <files>`: Creates a zip archive

### `unzip`
Extracts files from a zip archive.

- `unzip <archive_name>.zip`: Extracts a zip archive

## Searching

### `grep` (Global Regular Expression Print)
Searches for patterns in text.

- `grep "<pattern>" <file>`: Searches for the pattern in the file
- `grep -r "<pattern>" <directory>`: Searches recursively in a directory

**Example:** `grep "error" /var/log/syslog`

## File Comparison

### `diff` (Difference)
Compares two files line by line.

- `diff <file1> <file2>`: Shows the differences between the two files

### `cmp` (Compare)
Compares two files byte by byte.

- `cmp <file1> <file2>`: Shows the first differing byte position

### `comm` (Common)
Compares two sorted files.

- `comm <file1> <file2>`: Shows lines unique to each file and common lines

## Output Manipulation

### `head`
Displays the first few lines of a file.

- `head <file>`: Displays the first 10 lines
- `head -n <number> <file>`: Displays the specified number of lines

### `tail`
Displays the last few lines of a file.

- `tail <file>`: Displays the last 10 lines
- `tail -n <number> <file>`: Displays the specified number of lines
- `tail -f <file>`: Follows the file and displays new lines as they are added

### `sort`
Sorts lines in a file.

- `sort <file>`: Sorts lines alphabetically
- `sort -n <file>`: Sorts lines numerically

## Environment Variables

### `export`
Sets or displays environment variables.

- `export <variable>=<value>`: Sets an environment variable
- `export`: Displays all environment variables

## Networking

### `ssh` (Secure Shell)
Connects to a remote server securely.

- `ssh <username>@<hostname>`: Connects to the remote server

### `ifconfig` (Interface Configuration - deprecated, use ip)
Displays network interface information.

- `ifconfig`: Displays information about all network interfaces

### `traceroute`
Traces the route of network packets.

- `traceroute <hostname>`: Traces the route to the specified hostname

### `wget` (Web Get)
Downloads files from the internet.

- `wget <URL>`: Downloads the file from the specified URL

### `ufw` (Uncomplicated Firewall)
Manages the firewall (easier interface to iptables).

- `ufw enable`: Enables the firewall
- `ufw allow <port>`: Allows traffic on the specified port
- `ufw status`: Shows the firewall status

### `iptables`
Configures the Netfilter firewall (more complex).

## Package Management

### `apt` (Advanced Package Tool - Debian/Ubuntu)
Manages software packages.

- `apt update`: Updates the package list
- `apt install <package_name>`: Installs a package
- `apt remove <package_name>`: Removes a package

### `pacman` (Package Manager - Arch Linux)
Manages software packages.

- `pacman -S <package_name>`: Installs a package
- `pacman -R <package_name>`: Removes a package

### `yum` (Yellowdog Updater, Modified - CentOS/RHEL)
Manages software packages.

- `yum install <package_name>`: Installs a package
- `yum remove <package_name>`: Removes a package

### `rpm` (RPM Package Manager - Red Hat based)
Manages .rpm packages.

- `rpm -ivh <package_name>.rpm`: Installs an RPM package
- `rpm -qp <package_name>.rpm`: Queries an RPM package file
- `rpm -e <package_name>`: Removes an RPM package

## System Monitoring & Performance

### `top`
Displays real-time system processes and resource usage.

- `top`: Opens the real-time task manager

### `htop`
An enhanced version of `top` with more user-friendly interface.

- `htop`: Displays an interactive and colorful system monitoring tool

### `ps` (Process Status)
Displays information about active processes.

- `ps aux`: Displays all running processes
- `ps -ef`: Shows a detailed list of processes

### `kill`
Terminates processes by their PID (Process ID).

- `kill <pid>`: Kills a process with the given PID
- `kill -9 <pid>`: Forcefully kills a process

### `free`
Displays memory usage.

- `free`: Displays memory and swap usage

### `df`
Shows disk space usage.

- `df -h`: Displays disk space usage in a human-readable format

### `du`
Displays file and directory space usage.

- `du -sh <directory>`: Shows the total size of a directory

### `uptime`
Displays system uptime.

- `uptime`: Shows how long the system has been running

### `dmesg`
Displays kernel ring buffer messages.

- `dmesg`: Displays kernel-related messages

### `shutdown`
Shuts down or reboots the system.

- `shutdown -h now`: Shuts down the system immediately
- `shutdown -r now`: Reboots the system immediately

### `reboot`
Reboots the system.

- `reboot`: Reboots the system

## User Management

### `useradd`
Adds a new user.

- `useradd <username>`: Creates a new user

### `passwd`
Changes a user's password.

- `passwd <username>`: Changes the password for the specified user

### `usermod`
Modifies a user's account.

- `usermod -aG <group> <username>`: Adds a user to a group

### `userdel`
Deletes a user.

- `userdel <username>`: Deletes the user and its home directory (if specified)

### `groups`
Displays the groups a user belongs to.

- `groups <username>`: Displays the groups the user is a member of

### `chown`
Changes file ownership.

- `chown <owner>:<group> <file>`: Changes the owner and group of the file

### `chmod`
Changes file permissions.

- `chmod <permissions> <file>`: Changes the file permissions using symbolic or numeric modes

### `sudo`
Executes commands with superuser privileges.

- `sudo <command>`: Executes a command as a superuser

## File Permissions & Ownership

### `chmod` (Change Mode)
Modifies file or directory permissions.

- `chmod 755 <file>`: Assigns read, write, and execute permissions to the owner, and read and execute permissions to others
- `chmod +x <file>`: Adds execute permission for all users

### `chown` (Change Owner)
Changes the ownership of files or directories.

- `chown <user>:<group> <file>`: Changes the owner and group of the file or directory

### `chgrp` (Change Group)
Changes the group of a file or directory.

- `chgrp <group> <file>`: Changes the group of a file or directory

### `find`
Searches for files and directories based on conditions.

- `find <directory> -name <filename>`: Searches for files by name
- `find <directory> -type f -mtime -7`: Searches for files modified in the last 7 days

### `locate`
Searches for files by name quickly.

- `locate <filename>`: Searches for a file by its name using an index

### `updatedb`
Updates the locate database.

- `updatedb`: Updates the database used by the `locate` command

## Scripting & Automation

### `bash` (Bourne Again Shell)
The default shell for most Linux distributions.

- `bash`: Launches the Bash shell

### `sh` (Shell)
A command interpreter for Unix-like systems.

- `sh <script.sh>`: Executes a shell script
- `chmod +x <script.sh>`: Makes a script executable

### `crontab` (Cron Table)
Schedules jobs for periodic execution.

- `crontab -e`: Edits the crontab file to schedule jobs
- `crontab -l`: Lists scheduled jobs

### `at`
Schedules a one-time job.

- `at <time>`: Schedules a command to be executed at a specific time

### `alias`
Creates shortcuts for commands.

- `alias <shortcut>="<command>"`: Creates an alias for a command

### `unalias`
Removes an alias.

- `unalias <shortcut>`: Removes the defined alias

### `env`
Displays or sets environment variables.

- `env`: Displays environment variables
- `env <command>`: Runs a command with modified environment variables

## Miscellaneous

### `echo`
Displays text or outputs variable values.

- `echo $USER`: Displays the current user's username

### `history`
Displays the command history.

- `history`: Lists previous commands typed in the terminal

### `clear`
Clears the terminal screen.

- `clear`: Clears all content from the terminal window

### `exit`
Exits the terminal session.

- `exit`: Exits the terminal or logs out from the current session

---

This guide covers the essential Linux commands that every user should know. Practice these commands regularly to become proficient in Linux system administration and daily operations.
