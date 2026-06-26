**1\. File & Directory (Daily Use)**

**ls**

**Meaning:** List files and directories  
**Why:** View the contents of the current directory.  
**Example:** ls

**ls -l**

**Meaning:** List files and directories in long format  
**Why:** Display detailed information such as permissions, owner, size, and modification date.  
**Example:** ls -l

**cd**

**Meaning:** Change directory  
**Why:** Navigate from one directory to another.  
**Example:** cd Documents

**pwd**

**Meaning:** Print current working directory  
**Why:** Know your current location in the file system.  
**Example:** pwd

**mkdir**

**Meaning:** Make a new directory  
**Why:** Create a new folder.  
**Example:** mkdir Projects

**rm -r**

**Meaning:** Remove a directory and its contents recursively  
**Why:** Delete a folder along with all files and subdirectories inside it.  
**Example:** rm -r Projects

**cp**

**Meaning:** Copy files or directories  
**Why:** Create a duplicate of a file or folder.  
**Example:** cp file.txt backup.txt

**mv**

**Meaning:** Move or rename files and directories  
**Why:** Change a file's location or rename it.  
**Example:** mv file.txt Documents/

**touch**

**Meaning:** Create a new empty file or update a file's timestamp  
**Why:** Quickly create a file or modify its last accessed/modified time.  
**Example:** touch notes.txt

2\. File Reading (VERY IMPORTANT)

**cat**

**Meaning:** Concatenate and display file contents  
**Why:** View the entire contents of a small text file.  
**Example:** cat file.txt
using cat (to type multiple lines)
cat >file.txt
now type your text and press Ctrl+ D

**less**

**Meaning:** View file contents one page at a time  
**Why:** Read large files with easy forward and backward navigation.  
**Example:** less file.txt

**head**

**Meaning:** Display the first 10 lines of a file  
**Why:** Quickly check the beginning of a file.  
**Example:** head file.txt

**tail**

**Meaning:** Display the last 10 lines of a file  
**Why:** View the end of a file, such as recent log entries.  
**Example:** tail file.txt

**tail -f**

**Meaning:** Follow the end of a file in real time  
**Why:** Continuously monitor log files as new data is added.  
**Example:** tail -f /var/log/syslog

3\. Permissions (Must)

**chmod**

**Meaning:** Change file or directory permissions  
**Why:** Control who can read, write, or execute a file or directory.  
**Example:** chmod 755 script.sh

**chown**

**Meaning:** Change file or directory ownership  
**Why:** Assign a different user or group as the owner of a file or directory.  
**Example:** chown user:group file.txt

4\. Process Management

**ps -ef**

**Meaning:** Display all running processes in full format  
**Why:** View detailed information about active processes.  
**Example:** ps -ef

**top**

**Meaning:** Display real-time system and process information  
**Why:** Monitor CPU, memory usage, and running processes.  
**Example:** top

**kill**

**Meaning:** Terminate a process using its Process ID (PID)  
**Why:** Stop a running process gracefully.  
**Example:** kill 1234

**kill -9**

**Meaning:** Forcefully terminate a process using the SIGKILL signal  
**Why:** Immediately stop an unresponsive or stuck process.  
**Example:** kill -9 1234

5\. System & Memory

**df -h**

**Meaning:** Display disk space usage in human-readable format  
**Why:** Check available and used disk space on mounted file systems.  
**Example:** df -h

**free -m**

**Meaning:** Display memory usage in megabytes  
**Why:** Check RAM and swap memory usage.  
**Example:** free -m

**du -sh**

**Meaning:** Display the total size of a file or directory in human-readable format  
**Why:** Check how much disk space a file or directory occupies.  
**Example:** du -sh Documents/

Top of Form

6\. Networking (Very Important)

**ping**

**Meaning:** Check network connectivity to a host  
**Why:** Verify if a remote system is reachable and measure response time.  
**Example:** ping google.com

**curl**

**Meaning:** Transfer data from or to a server  
**Why:** Test APIs, download files, or retrieve web page content.  
**Example:** curl <https://example.com>

**wget**

**Meaning:** Download files from the internet  
**Why:** Retrieve files from web servers using HTTP, HTTPS, or FTP.  
**Example:** wget <https://example.com/file.zip>

**netstat**

**Meaning:** Display network connections and listening ports  
**Why:** Check active connections, open ports, and network statistics.  
**Example:** netstat -tuln

**ssh**

**Meaning:** Securely connect to a remote system  
**Why:** Access and manage another computer over a secure encrypted connection.  
**Example:** ssh user@192.168.1.10

7\. Package Management

**apt install**

**Meaning:** Install a software package using APT  
**Why:** Download and install a package on Debian-based Linux distributions such as Ubuntu.  
**Example:** sudo apt install nginx

**apt update**

**Meaning:** Update the package list from repositories  
**Why:** Refresh the list of available packages and their latest versions before installing or upgrading software.  
**Example:** sudo apt update

**yum install**

**Meaning:** Install a software package using YUM  
**Why:** Download and install a package on Red Hat-based Linux distributions such as CentOS.  
**Example:** sudo yum install httpd

8\. Services

**systemctl start**

**Meaning:** Start a system service  
**Why:** Launch a service without rebooting the system.  
**Example:** sudo systemctl start nginx

**systemctl stop**

**Meaning:** Stop a system service  
**Why:** Stop a running service safely.  
**Example:** sudo systemctl stop nginx

**systemctl restart**

**Meaning:** Restart a system service  
**Why:** Apply changes or recover a service by stopping and starting it again.  
**Example:** sudo systemctl restart nginx

**systemctl status**

**Meaning:** Display the status of a system service  
**Why:** Check whether a service is running and view recent log information.  
**Example:** systemctl status nginx

Top of Form

Bottom of Form

Top of Form

9\. User & Access

**whoami**

**Meaning:** Display the current logged-in user  
**Why:** Know which user account is currently active.  
**Example:** whoami

**useradd**

**Meaning:** Create a new user account  
**Why:** Add a new user to the Linux system.  
**Example:** sudo useradd john

**passwd**

**Meaning:** Change or set a user password  
**Why:** Create or update a password for a user account.  
**Example:** sudo passwd john

Top of Form

10\. Search & Filters (Advanced but Important)

**grep**

**Meaning:** Search for a specific pattern or text inside files  
**Why:** Find matching words or lines quickly in files or command output.  
**Example:** grep "error" log.txt

**find**

**Meaning:** Search for files and directories  
**Why:** Locate files based on name, type, size, or other conditions.  
**Example:** find /home -name file.txt

**grep "error" logfile.log** 👉 Very powerful in real work 🚀

👉 You will:

- Check logs → tail -f ✅
- Check process → ps -ef ✅
- Restart service → systemctl restart ✅

👉 That's real DevOps work 💯

Top of Form

Bottom of Form

Bottom of Form

Bottom of Form

Top of Form

Bottom of Form

Bottom of Form

Top of Form

Bottom of Form

Top of Form

Bottom of Form

Top of Form

Bottom of Form
