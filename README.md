# Linux/Unix Command Cheatsheet

A comprehensive cheatsheet for common Linux and Unix commands.

## 1. System Information

| Command | Description |
| :--- | :--- |
| `uname -a` | Display Linux system information. |
| `uname -r` | Display kernel release information. |
| `hostname` | Show system host name. |
| `hostname -I` | Display the IP addresses of the host. |
| `last reboot` | Show system reboot history. |
| `date` | Show the current date and time. |
| `cal` | Show this month's calendar. |
| `w` | Display who is online. |
| `whoami` | Who you are logged in as. |

## 2. Hardware Information

| Command | Description |
| :--- | :--- |
| `cat /proc/cpuinfo` | Display CPU information. |
| `cat /proc/meminfo` | Display memory information. |
| `hdparm -i /dev/sda` | Show info about disk sda. |

## 3. Performance Monitoring

| Command | Description |
| :--- | :--- |
| `top` | Display and manage the top processes. |
| `htop` | Interactive process viewer (top alternative). |
| `mpstat 1` | Display processor related statistics. |
| `vmstat 1` | Display virtual memory statistics. |
| `iostat 1` | Display I/O statistics. |
| `tail 100 /var/log/messages` | Display the last 100 syslog messages. |
| `tcpdump -i eth0 'port 80'` | Monitor all traffic on port 80. |

## 4. File and Directory Commands

| Command | Description |
| :--- | :--- |
| `ls -al` | List all files in a long listing (detailed) format. |
| `pwd` | Display the present working directory. |
| `mkdir directory` | Create a directory. |
| `rm file` | Remove (delete) file. |
| `rm -r directory` | Remove the directory and its contents recursively. |
| `rm -f file` | Force removal of file without prompting. |
| `rm -rf directory` | Forcefully remove directory recursively. |
| `cp file1 file2` | Copy file1 to file2. |
| `cp -r source_directory destination` | Copy source_directory recursively to destination. |
| `mv file1 file2` | Rename or move file1 to file2. |
| `ln -s /path/to/file linkname` | Create symbolic link to linkname. |
| `touch file` | Create an empty file or update the access/modification times. |
| `cat file` | View the contents of file. |
| `less file` | Browse through a text file. |
| `head file` | Display the first 10 lines of file. |
| `tail file` | Display the last 10 lines of file. |
| `tail -f file` | Display the last 10 lines of file and "follow" the file as it grows. |

## 5. Process Management

| Command | Description |
| :--- | :--- |
| `ps` | Display your currently running processes. |
| `ps -ef` | Display all the currently running processes on the system. |
| `kill pid` | Kill process with process ID of pid. |
| `killall processname` | Kill all processes named processname. |

## 6. File Permissions

| Permission | Example |
| :--- | :--- |
| `rwx rwx rwx` | `chmod 777 filename` |
| `rwx rwx r-x` | `chmod 775 filename` |
| `rwx r-x r-x` | `chmod 755 filename` |
| `rw- rw- r--` | `chmod 664 filename` |
| `rw- r-- r--` | `chmod 644 filename` |

-   `r` = Read
-   `w` = Write
-   `x` = execute
-   `-` = no access

## 7. Networking

| Command | Description |
| :--- | :--- |
| `ifconfig -a` | Display all network interfaces and ip address. |
| `ifconfig eth0` | Display eth0 address and details. |
| `ethtool eth0` | Query or control network driver and hardware settings. |
| `ping host` | Send ICMP echo request to host. |
| `whois domain` | Display whois information for domain. |
| `dig domain` | Display DNS information for domain. |

## 8. Archives (Tar)

| Command | Description |
| :--- | :--- |
| `tar cf archive.tar directory` | Create tar named archive.tar containing directory. |
| `tar xf archive.tar` | Extract the contents from archive.tar. |
| `tar czf archive.tar.gz directory` | Create a gzip compressed tar file name archive.tar.gz. |
| `tar xzf archive.tar.gz` | Extract a gzip compressed tar file. |
| `tar cjf archive.tar.bz2 directory` | Create a tar file with bzip2 compression. |
| `tar xjf archive.tar.bz2` | Extract a bzip2 compressed tar file. |

## 9. Search

| Command | Description |
| :--- | :--- |
| `grep pattern file` | Search for pattern in file. |
| `grep -r pattern directory` | Search recursively for pattern in directory. |
| `locate name` | Find files and directories by name. |
| `find /home/john -name 'prefix*'` | Find files in /home/john that start with "prefix". |
| `find /home -size +100M` | Find files larger than 100MB in /home. |

## 10. SSH

| Command | Description |
| :--- | :--- |
| `ssh host` | Connect to host as your local username. |
| `ssh user@host` | Connect to host as user. |
| `ssh -p port user@host` | Connect to host using port. |

## 11. File Transfer

| Command | Description |
| :--- | :--- |
| `scp file.txt server:/tmp` | Secure copy file.txt to the /tmp folder on server. |
| `scp server:/var/www/*.html /tmp` | Copy \*.html files from server to the local /tmp folder. |
| `scp -r server:/var/www /tmp` | Copy all files and directories recursively from server to the current system's /tmp folder. |
| `rsync -a /home /backups/` | Synchronize /home to /backups/home. |
| `rsync -avz /home server:/backups/` | Synchronize files/directories between the local and remote system with compression enabled. |

## 12. User Management

| Command | Description |
|:---|:---|
| `who` | Show who is currently logged in. |
| `sudo adduser username` | Create a new user account on the system with the specified username. |
| `finger` | Display information about all the users currently logged into the system, including their usernames, login time, and terminal. |
| `sudo deluser USER GROUPNAME` | Remove the specified user from the specified group. |
| `last` | Show the recent login history of users. |
| `finger username` | Provide information about the specified user, including their username, real name, terminal, idle time, and login time. |
| `sudo userdel -r username` | Delete the specified user account from the system, including their home directory and associated files. The -r option ensures the removal of the user's files. |
| `sudo passwd -l username` | Lock the password of the specified user account, preventing the user from logging in. |
| `su - username` | Switch to another user account with the user's environment. |
| `sudo usermod -a -G GROUPNAME USERNAME` | Add an existing user to the specified group. The user is added to the group without removing them from their current groups. |
