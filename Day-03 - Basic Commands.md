## Linux Concepts

#### Basis Linux Commands: 

Here are some basic and most commonly used Linux commands in a simple format:

#### File & Directory Commands

| Command            | Meaning                                     |
| ------------------ | ------------------------------------------- |
| ls                 | List files and folders in current directory |
| ls -l              | List with details (permissions, size)       |
| ls -a              | Show hidden files also                      |
| pwd                | Show current directory path                 |
| cd foldername      | Change directory                            |
| cd ..              | Go one step back (parent folder)            |
| mkdir foldername   | Create a new folder                         |
| rmdir foldername   | Remove an empty folder                      |
| rm filename        | Delete a file                               |
| rm -r foldername   | Delete a folder and its files               |
| cp file1 file2     | Copy a file                                 |
| cp -r src dst      | Copy a folder                               |
| mv old new         | Move or rename file/folder                  |
| cat                | Display the content of a file               |
| echo               | Print text or message on screen             | 
| tee              | Takes output from another command and copies it to a file while still showing it on screen.     | 

#### File Handling

| Command          | Meaning                     |
| ---------------- | --------------------------- |
| touch filename   | Create an empty file        |
| cat filename     | Show file content           |
| more filename    | View file page by page      |
| less filename    | View file page by page      |
| head filename    | Show first 10 lines         |
| tail filename    | Show last 10 lines          |

#### Disk & system Monitoring

| Command  | Meaning                                  |
| -------- | ---------------------------------------- |
| df       | Show available disk space                |
| du       | Show disk usage of files and directories |
| top      |  Shows running processes and CPU/RAM usage live  |
| free     | Shows memory (RAM) and swap usage in the system  | 


#### What is SSH?

SSH stands for Secure Shell. It’s a network protocol that allows you to:

1. Securely connect to a remote computer (like a server) over an unsecured network.
2. Run commands remotely on that server.
3. Transfer files securely between computers.

#### Key Points:
SSH uses port 22 by default.
1. Authentication can be done with:
2. Password and SSH keys (more secure, preferred for servers).

#### How to Use SSH

```
ssh john@192.168.1.100
```

#### What is SCP?

1. SCP stands for Secure Copy Protocol.
2. It’s a command-line tool that allows you to:
3. Copy files and directories securely between a local and a remote machine or between two remote machines.
4. Use SSH encryption, so the file transfer is secure.

#### Local to Remote server - In windows
```
scp -i "C:\Users\9196\Downloads\linux.pem" file.txt vibhuti@127.34.0.0:/home/vibhuti
```

#### Remote to Windows - In windows
```
scp -i "C:\Users\91916\downloads\linux.pem" ubuntu@3.137.162.91:/home/ubuntu/file.txt .
```

