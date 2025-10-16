## **Linux Essentials: A Step-by-Step Command Guide by LuxDevHQ**

### Basic SSH connection
SSH (Secure Shell) lets you open an encrypted terminal session to a remote machine, typically with ssh <username>@<server_address>. On first connect, you’ll be asked to verify the server’s host key, then authenticate with a password or—preferably—an SSH key you created with ssh-keygen and installed via ssh-copy-id. If the server uses a custom port, add -p <port>, and if you need a specific key file, use -i <path_to_private_key>. For convenience, you can define a short alias in ~/.ssh/config so you can just run ssh myserver.

```
ssh <username>@<server_address>
```

>> Example: connect as user 'ubuntu' to server at 203.0.113.10
```
ssh ubuntu@203.0.113.10
```

>> If the server uses a custom port (e.g., 2222)
```
ssh -p 2222 <username>@<server_address>
```

>> Using a specific private key
>>
```
ssh -i ~/.ssh/id_ed25519 <username>@<server_address>
```
---
### File & Directory Management

#### **`ls` (List)**  
Lists directory contents.  

- `ls` → Lists files and directories in the current directory  
- `ls -l` → Long format (permissions, owner, size, etc.)  
- `ls -a` → Shows hidden files (dotfiles)  
- `ls -lh` → Human-readable sizes (KB, MB, GB)  

**Example:** `ls -l /home/user/documents`

---

#### **`pwd` (Print Working Directory)**  
Displays the current directory path.  

- `pwd` → Prints the absolute path  

---

#### **`cd` (Change Directory)**  
Navigates through directories.  

- `cd <directory_path>` → Moves to directory  
- `cd ..` → Goes up one level  
- `cd` → Returns to home  

**Example:** `cd /var/log`

---

#### **`mkdir` (Make Directory)**  
Creates new directories.  

- `mkdir <directory_name>` → Makes directory  
- `mkdir -p <path>` → Creates parent directories  

**Example:** `mkdir new_folder`

---

#### **`mv` (Move/Rename)**  
Moves or renames files and directories.  

- `mv old_file.txt new_file.txt` → Rename  
- `mv file.txt /tmp` → Move  

---

#### **`cp` (Copy)**  
Copies files and directories.  

- `cp <source> <destination>` → Copy file  
- `cp -r <src_dir> <dest_dir>` → Copy directory recursively  

**Example:** `cp file.txt file_copy.txt`

---

#### **`rm` (Remove)**  
Deletes files or directories.  

- `rm <file>` → Delete file  
- `rm -r <dir>` → Delete recursively (dangerous!)  
- `rm -i <file>` → Confirm before delete  

---

#### **`touch`**  
Creates empty files or updates timestamps.  

- `touch file.txt`

---

#### **`ln` (Link)**  
Creates symbolic or hard links.  

- `ln -s <source> <link>` → Symbolic link  
- `ln <source> <link>` → Hard link  

---

#### **`clear`**  
Clears the terminal screen.  

---

### Viewing & Editing Files

#### **`cat` (Concatenate)**  
Displays file contents.  

- `cat file.txt`

---

#### **`echo`**  
Prints text or variables.  

- `echo "Hello Linux"`  
- `echo $USER`  

---

### **`less`**  
Views file one page at a time.  

- `less file.txt` → Scrollable, press `q` to exit  

---

#### **`man` (Manual)**  
Shows documentation.  

- `man ls`  

---

### System Information

#### **`uname` (Unix Name)**  
Displays system info.  

- `uname -a` → Full details  
- `uname -r` → Kernel release  

---

### **`whoami`**  
Shows current username.  

---

## Archives & Compression

### **`tar` (Tape Archive)**  
Create/extract archives.  

- `tar -cvf file.tar files/` → Create  
- `tar -xvf file.tar` → Extract  

---

### **`zip` / `unzip`**  
Compress/extract zip files.  

- `zip archive.zip file1 file2`  
- `unzip archive.zip`  

---

## Searching

### **`grep` (Search in files)**  
Searches text patterns.  

- `grep "error" syslog`  
- `grep -r "main()" src/`  

---

## File Comparison

### **`diff`**  
Compares files line by line.  

- `diff file1 file2`  

### **`cmp`**  
Compares files byte by byte.  

### **`comm`**  
Compares sorted files.  

---

## Output Manipulation

### **`head` / `tail`**  
Show first/last lines.  

- `head -n 20 file.txt`  
- `tail -f logfile`  

---

### **`sort`**  
Sorts lines.  

- `sort file.txt`  

---

## Environment Variables

### **`export`**  
Set or list variables.  

- `export PATH=$PATH:/new/path`  

---

## Networking

### **`ssh`**  
Remote login.  

- `ssh user@host`  

### **`ifconfig` / `ip addr`**  
Show interfaces.  

### **`traceroute`**  
Trace network hops.  

### **`wget`**  
Download files.  

- `wget https://example.com/file`  

### **`ufw` / `iptables`**  
Firewall management.  

---

## Package Management

### **`apt` (Debian/Ubuntu)**  
- `apt update`  
- `apt install nginx`  

### **`pacman` (Arch)**  
- `pacman -S package`  

### **`yum` (RHEL/CentOS)**  
- `yum install package`  

### **`rpm`**  
- `rpm -ivh package.rpm`  

---

## System Monitoring & Performance

### **`top` / `htop`**  
Process monitoring.  

### **`ps`**  
Show processes.  

- `ps aux`  

### **`kill`**  
End process.  

- `kill -9 PID`  

### **`free`**  
Show memory usage.  

### **`df` / `du`**  
Disk usage.  

- `df -h`  
- `du -sh /var`  

### **`uptime`**  
System uptime.  

### **`dmesg`**  
Kernel messages.  

### **`shutdown` / `reboot`**  
System power control.  

---

## User Management

### **`useradd` / `userdel`**  
Add/remove user.  

### **`passwd`**  
Change password.  

### **`usermod`**  
Modify user.  

- `usermod -aG sudo user`  

### **`groups`**  
List groups.  

### **`chown` / `chmod` / `chgrp`**  
Ownership and permissions.  

- `chmod 755 script.sh`  

### **`sudo`**  
Run as root.  

---

## File Permissions & Ownership

### **`find`**  
Search files.  

- `find / -name "*.conf"`  

### **`locate` / `updatedb`**  
Indexed search.  

---

## Scripting & Automation

### **`bash` / `sh`**  
Run shell scripts.  

### **`crontab` / `at`**  
Schedule tasks.  

### **`alias` / `unalias`**  
Command shortcuts.  

### **`env`**  
Show environment variables.  

---

## Miscellaneous

### **`history`**  
Command history.  

### **`clear`**  
Clear screen.  

### **`exit`**  
Exit session.  

---
