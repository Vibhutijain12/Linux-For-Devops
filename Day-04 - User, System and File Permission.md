### Linux Concepts

#### 1. System level commands: 

Here are some basic and most commonly used Linux commands in a simple format:

| Command                                 | Meaning                                                         |
| --------------------------------------- | --------------------------------------------------------------- |
| cat /etc/os-release                   | Shows the information about OS of the Linux.                      |
| uname -a                              | Shows system information (kernel, architecture, OS).            |
| top                                   | Displays real-time running processes and system resource usage. |
| htop                                  | Enhanced version of top (interactive, colorful).              |
| df -h                                 | Shows disk space usage in human-readable format.                |
| du -sh <dir>                          | Shows disk usage of a directory.                                |
| free -h                               | Displays memory (RAM) usage.                                    |
| ps aux                                | Shows all running processes.                                    |
| kill <PID>                            | Kills a running process by process ID.                          |
| shutdown -h now                       | Immediately shuts down the system.                              |
| reboot                                | Restarts the system.                                            |
| systemctl status <service>            | Shows status of a system service.                               |
| systemctl start/stop/enable <service> | Manage system services.                       |
| uptime                             | Shows how long the system has been running, the number of users logged in, and the system load average.                              | 
| who                                | Shows all users currently logged into the system, along with login time, terminal, and source. |
| whoami                             | Displays the current logged-in user's username. | 
| which                              | Shows the full path of a command/executable that will run when you type it.   | 

#### 2. User Management commands

| Command                      | Meaning                                        |
| ---------------------------- | ---------------------------------------------- |
| useradd <username>         | Creates a new user.                            |
| passwd <username>          | Sets or changes the user password.             |
| userdel <username>         | Deletes a user.                                |
| groupadd <groupname>       | Creates a new group.                           |
| usermod -aG <group> <user> | Adds a user to a group.                        |
| id <username>              | Shows user ID, group ID, and group membership. |
| groupdel                   | Deletes the group  |
| su - <username>            | Switches to another user account.              |
| sudo <command>             | Runs a command as the superuser.               |
| cat /etc/groups            | system file that stores group information.          | 
| cat /etc/passwd            | system file that stores user account information.    |   
| gpasswd -a <username> <groupname>  | Adds a user to a group.                   | 
| gpasswd -M <USER1><USER2><USER3> <groupname> | Sets (replaces) the entire list of group members.  | 

#### 3. File permission commands: 

Linux file permissions include:

1. r = read
2. w = write
3. x = execute

##### For three groups: owner, group, others

#### Check permissions

| Command | Meaning                                       |
| ------- | --------------------------------------------- |
| ls -l | Shows detailed file listing with permissions. |

| Command            | Meaning                                  |
| ------------------ | ---------------------------------------- |
| chmod 755 <file> | Sets permissions using numbers.          |
| chmod u+x <file> | Adds execute permission to the owner.    |
| chmod g-w <file> | Removes write permission from the group. |
| chmod o-r <file> | Removes read permission from others.     |

#### Change ownership

| Command                       | Meaning                       |
| ----------------------------- | ----------------------------- |
| `chown <user> <file>`         | Changes owner of a file.      |
| `chown <user>:<group> <file>` | Changes owner and group.      |
| `chgrp <group> <file>`        | Changes only group ownership. |

#### Compression & Decompression Commands

1. tar -  
Commonly used to archive & compress directories.


| Command                       | Meaning                     |
| ----------------------------- | --------------------------- |
| tar -czvf file.tar.gz dir/  | Create gzip compressed tar. |
| tar -xzvf file.tar.gz       | Extract gzip tar file.      |

2. zip / unzip - 

| Command                | Meaning                     |
| ---------------------- | --------------------------- |
| zip file.zip folder/  | Compress a folder into zip. |
| unzip file.zip       | Extract zip file.           |
