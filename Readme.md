# Open Source Audit — Git  

##  Student Information  

* Name: Mahak Mathuriya  
* Registration Number: 24BCY10135  
* Course: Open Source Software  
* Project Title: Open Source Audit  

---  

##  Chosen Software: Git  

Git is a distributed version control system created by Linus Torvalds in 2005. It helps developers manage and track changes in source code efficiently. It also allows multiple users to collaborate on the same project while maintaining a proper history of all updates.  

---  

##  Project Objective  

The objective of this project is to:  

* Analyze an open-source software (Git)  
* Understand its origin, license, and working concept  
* Study its behavior on a Linux system  
* Explore the FOSS ecosystem  
* Implement Linux shell scripts demonstrating automation and system interaction  

---  

##  What is Git? (Working Overview)  

Git works on a distributed model, meaning:  

* Every user has a complete copy of the repository  
* Changes are tracked using commits  
* Collaboration happens via push, pull, and merge operations  

###  Basic Workflow:  

```  
git init        # Initialize repository  
git add .       # Stage changes  
git commit -m "message"   # Save snapshot  
git push        # Upload to remote repo  
```  

---  

##  System Requirements  

###  Hardware Requirements  

* Minimum 2GB RAM  
* 10GB free disk space  

### Software Requirements  

* Linux OS (Ubuntu recommended)  
* Bash shell  
* Git installed  

---  

##  Installation Guide  

###  Step 1: Update system packages  

```  
sudo apt update  
sudo apt upgrade -y  
```  

###  Step 2: Install required packages  

```  
sudo apt install git -y  
```  

###  Step 3: Verify installation  

```  
git --version  
```  

Expected output:  

```  
git version 2.x.x  
```  

---  

##  Project Structure  

```  
oss-audit-24BCY10135/  
│  
├── README.md  
├── script1.sh  
├── script2.sh  
├── script3.sh  
├── script4.sh  
└── script5.sh  
```  

---  

##  Shell Scripts — Detailed Explanation  

---  

###  Script 1: System Identity Report  

####  Purpose:  

Displays basic system information such as:  

* Kernel version  
* Logged-in user  
* Linux distribution  
* Uptime  
* Date and time  
* Open source license  

####  Concepts Used:  

* Variables  
* Command substitution ($())  
* echo formatting  

####  How it works:  

The script collects system information using Linux commands like:  

* uname -r → Kernel version  
* whoami → Current user  
* uptime -p → System uptime  
* lsb_release -d → Distribution info

'''
#!/bin/bash

echo "----- System Identity Report -----"

kernel=$(uname -r)
user=$(whoami)
distro=$(lsb_release -d | cut -f2)
uptime=$(uptime -p)
datetime=$(date)

echo "Kernel Version: $kernel"
echo "User: $user"
echo "Distribution: $distro"
echo "Uptime: $uptime"
echo "Date & Time: $datetime"
echo "License: Open Source (GPL)"
''' 

---  

###  Script 2: FOSS Package Inspector  

####  Purpose:  

* Checks if Git is installed  
* Displays version and package details  
* Prints a philosophy statement  

####  Concepts Used:  

* if-else condition  
* case statement  
* dpkg package manager  
* grep and pipes  

####  How it works:  

* Uses dpkg -l to check installation  
* Extracts details using dpkg -s  
* Uses case to print software description  

---  

###  Script 3: Disk and Permission Auditor  

####  Purpose:  

* Checks system directories  
* Displays:  
  * Permissions  
  * Owner  
  * Disk usage  

####  Concepts Used:  

* for loop  
* array handling  
* awk  
* du and ls commands  

####  How it works:  

* Loops through predefined directories  
* Extracts permissions using ls -ld  
* Calculates size using du -sh  

---  

###  Script 4: Log File Analyzer  

####  Purpose:  

* Reads log files  
* Counts occurrences of a keyword (default: "error")  

####  Concepts Used:  

* while loop  
* if condition  
* command-line arguments  
* counters  

####  How it works:  

* Reads file line-by-line  
* Matches keyword using grep  
* Counts occurrences  
* Displays last 5 matching lines  

---  

###  Script 5: Open Source Manifesto Generator  

####  Purpose:  

* Generates a personalized open-source statement  

####  Concepts Used:  

* user input (read)  
* string concatenation  
* file handling  

####  How it works:  

* Takes 3 inputs from user  
* Combines them into a paragraph  
* Saves output to a .txt file  

---  

##  How to Run the Project  

### Step 1: Clone repository  

```  
git clone <https://github.com/Mahak-7581/oss_audit_24bcy10135>  
cd oss-audit-24BCY10135  
```  

### Step 2: Give execution permission  

```  
chmod +x *.sh  
```  

### Step 3: Execute scripts  

```  
./script1.sh  
./script2.sh  
./script3.sh  
./script4.sh /var/log/syslog error  
./script5.sh  
```  

---  

##  Key Linux Concepts Demonstrated  

* File permissions  
* Package management  
* Shell scripting basics  
* Process of automation  
* Log file analysis  

---  


##  Conclusion  

This project demonstrates how open-source tools like Git help developers work efficiently with transparency and flexibility. It also provides practical knowledge of Linux and shell scripting along with theoretical understanding.
