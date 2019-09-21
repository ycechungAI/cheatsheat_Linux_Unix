# cheatsheat_Linux_Unix
My personal cheatsheat for learning Linux/Unix

1. System
#===============================
# Display Linux system information
uname -a

# Display kernel release information
uname -r

# Show system host name
hostname

# Display the IP addresses of the host
hostname -I

# Show system reboot history
last reboot

# Show the current date and time
date

# Show this month's calendar
cal

# Display who is online
w

# Who you are logged in as
whoami

2. Hardware Information
#===============================
# Display CPU information
cat /proc/cpuinfo

# Display memory information
cat /proc/meminfo

# Show info about disk sda
hdparm -i /dev/sda

3. Performance Monitoring
#===============================
# Display and manage the top processes
top

# Interactive process viewer (top alternative)
htop

# Display processor related statistics
mpstat 1

# Display virtual memory statistics
vmstat 1

# Display I/O statistics
iostat 1

# Display the last 100 syslog messages  (Use /var/log/syslog for Debian based systems.)
tail 100 /var/log/messages

# Monitor all traffic on port 80 ( HTTP )
tcpdump -i eth0 'port 80'

4. File and Directory Commands
================================
# List all files in a long listing (detailed) format
ls -al

# Display the present working directory
pwd

# Create a directory
mkdir directory

# Remove (delete) file
rm file

# Remove the directory and its contents recursively
rm -r directory

# Force removal of file without prompting for confirmation
rm -f file

# Forcefully remove directory recursively
rm -rf directory

# Copy file1 to file2
cp file1 file2

# Copy source_directory recursively to destination. If destination exists, copy source_directory into destination, otherwise create destination with the contents of source_directory.
cp -r source_directory destination

# Rename or move file1 to file2. If file2 is an existing directory, move file1 into directory file2
mv file1 file2

# Create symbolic link to linkname
ln -s /path/to/file linkname

# Create an empty file or update the access and modification times of file.
touch file

# View the contents of file
cat file

# Browse through a text file
less file

# Display the first 10 lines of file
head file

# Display the last 10 lines of file
tail file

# Display the last 10 lines of file and "follow" the file as it grows.
tail -f file

5. Process Management
#=============================
# Display your currently running processes
ps

# Display all the currently running processes on the system.
ps -ef

# Kill process with process ID of pid
kill pid

# Kill all processes named processname
killall processname

6. File Permission
#=============================
PERMISSION                  EXAMPLE

        Usr   Group  World
        rwx   rwx   rwx     chmod 777 filename
        rwx   rwx   r-x     chmod 775 filename
        rwx   r-x   r-x     chmod 755 filename
        rw-   rw-   r--     chmod 664 filename
        rw-   r--   r--     chmod 644 filename
        
r = Read
w = Write
x = execute
- = no access

7.Networking
#=============================
# Display all network interfaces and ip address
ifconfig -a

# Display eth0 address and details
ifconfig eth0

# Query or control network driver and hardware settings
ethtool eth0

# Send ICMP echo request to host
ping host

# Display whois information for domain
whois domain

# Display DNS information for domain
dig domain
 
8. Archives Tar
#=============================
# Create tar named archive.tar containing directory.
tar cf archive.tar directory

# Extract the contents from archive.tar.
tar xf archive.tar

# Create a gzip compressed tar file name archive.tar.gz.
tar czf archive.tar.gz directory

# Extract a gzip compressed tar file.
tar xzf archive.tar.gz

# Create a tar file with bzip2 compression
tar cjf archive.tar.bz2 directory

# Extract a bzip2 compressed tar file.
tar xjf archive.tar.bz2

9. Search
#============================
# Search for pattern in file
grep pattern file

# Search recursively for pattern in directory
grep -r pattern directory

# Find files and directories by name
locate name

# Find files in /home/john that start with "prefix".
find /home/john -name 'prefix*'

# Find files larger than 100MB in /home
find /home -size +100M

10. SSH
#=============================
# Connect to host as your local username.
ssh host

# Connect to host as user
ssh user@host

# Connect to host using port
ssh -p port user@host

11. FIle Transfer
#============================
# Secure copy file.txt to the /tmp folder on server
scp file.txt server:/tmp

# Copy *.html files from server to the local /tmp folder.
scp server:/var/www/*.html /tmp

# Copy all files and directories recursively from server to the current system's /tmp folder.
scp -r server:/var/www /tmp

# Synchronize /home to /backups/home
rsync -a /home /backups/

# Synchronize files/directories between the local and remote system with compression enabled
rsync -avz /home server:/backups/

Source: Course Notes && https://www.linuxtrainingacademy.com/linux-commands-cheat-sheet/



