## Linux Concepts

1. What is Linux?
2. Advantages of Linux? 
3. Architecture of Linux? 
4. What are the Kernel, Bootloader, and Shell? 
5. Difference between Linux and Windows. 
6. How to install Linux? 
7. What is Open Source? 
8. What is a file system in Linux? 

#### 1. What is Linux? 
Linux is an operating system that sits in the middle of hardware and the user. The user can run the application, and it takes the commands from the user and translates them to hardware.

#### 2. Advantages of Linux? 
1. Open source and used in 91% of the applications on the internet.
2. Allow multiple users to carry out multiple tasks and come up with powerful shells and multiple flavours.
3. Provides high security and doesn’t need any anti-virus software.

#### 3. Architecture of Linux? 

<img width="515" height="364" alt="image" src="https://github.com/user-attachments/assets/e022afd9-f9b9-4009-98a7-e521cb6e1fc9" />

The main components of the Linux operating system are: Application, Shell, Kernel, Hardware, and Utilities

#### 1. Kernel - 
The Kernel is the heart of Linux; it is responsible for all the major activities of the OS. It consists of all the programs, files, and processes required to run the OS.

#### 2. Shell - 
Shell is the program that connects our application to the kernel, like a mediator or gateway, through shell commands.

#### 3. Hardware Layer
The hardware layer of Linux is the lowest level of the operating system track. It plays a vital role in managing all the hardware components.

It includes device drivers, kernel functions, memory management, CPU control, and I/O operations. 

#### 4. What are the Kernel, Bootloader, and Shell? 

1. Kernel - The Kernel is the heart of Linux; it is responsible for all the major activities of the OS.

It consists of all the programs, files, and processes required to run the OS. 

It has separate memory or space to work with the OS, which helps to work wisely between hardware and software without interruption.

2. Shell - Shell is the program that connects our application to the kernel, like a mediator or gateway, through shell commands.
```
             SOFTWARE —> SHELL —--> KERNEL—-----> HARDWARE
```
3. Bootloader - Bootloader is one of the processes of the kernel that starts our operating system. It plays a pivotal role in initiating the system and facilitating the loading of the Linux kernel.
```
          Example - GRUB (Grand Unified Bootloader). 
```

#### 5. The difference between Linux and Windows. 

| Feature                   | **Linux**                                                 | **Windows**                                |
| ------------------------- | --------------------------------------------------------- | ------------------------------------------ |
| **Cost**                  | Mostly free and open-source                               | Paid / Licensed operating system           |
| **Source Code**           | Open-source → anyone can see/modify                       | Closed-source → only Microsoft controls it |
| **Customization**         | Highly customizable (themes, desktop environment, kernel) | Limited customization                      |
| **Security**              | Very secure, fewer viruses                                | More vulnerable to malware & viruses       |
| **Performance**           | Fast, lightweight, can run on old hardware                | Requires more resources (RAM, CPU)         |
| **User Control**          | Full control through terminal                             | More graphical, less backend control       |

#### 6. How to install Linux? 
We can install Linux in several ways:
###### 1. WSL
###### 2. On Cloud Provider (AWS, Azure, GCP)
###### 3. VM (Virtual Machines)

#### 7. What is Open Source? 
Open-source refers to something that people can contribute to and modify, making the design publicly accessible.

#### 8. What is a file system in Linux? 

A file system in Linux is the way files and folders are organized and stored on a computer.

Think of it like a big tree:

###### 1. The root of the tree is / (a single forward slash)

###### 2. Everything in Linux starts from /

###### 3. Inside it, there are branches (folders) and leaves (files).

| Folder  | What it contains (simple explanation)             |
| ------- | ------------------------------------------------- |
| `/`     | The root — the top of everything                  |
| `/home` | Your personal files (documents, music, downloads) |
| `/bin`  | Basic programs/commands (like `ls`, `cp`, `mv`)   |
| `/etc`  | System settings and configuration files           |
| `/dev`  | Files that represent hardware devices             |
| `/tmp`  | Temporary files                                   |
| `/usr`  | Installed software and user applications          |
| `/var`  | Files that keep changing (logs, cache)            |
| `/lib`  | Shared libraries needed by programs (like system files)    |
