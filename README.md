# 🔐 Cybersecurity &amp; Ethical Hacking Lab Environment Setup


###      Setting Up a Cybersecurity Lab Environment Using VirtualBox and Kali Linux
          

## 📌 Project Overview

This project focuses on setting up a virtual cybersecurity and penetration-testing laboratory using VirtualBox and Kali Linux.

The purpose of the lab is to create a controlled environment where cybersecurity tools, penetration testing, network scanning, reconnaissance, vulnerability assessment, and other security-testing activities can be performed safely and repeatedly.

The lab is configured on a private virtual network so that additional machines can be added later and used as targets for authorized security testing.

## 🎯 Objectives

The main objectives of this project are to:

Install and configure VirtualBox.
Install/import Kali Linux as a virtual machine.
Create a private NAT Network for the cybersecurity lab.
Configure network connectivity for Kali Linux.
Assign a consistent IP address to the Kali VM.
Verify network connectivity and DNS resolution.
Take a clean VM snapshot for recovery.
Document the complete setup process.
Prepare the environment for future cybersecurity projects.

## 🛡️ Purpose of the Lab

The lab provides an isolated and controlled environment for cybersecurity learning and authorized security testing.

It can be used for activities such as:

Network reconnaissance
Scanning and Enummeration
Vulnerability assessment
Packet analysis
Web security testing
Exploitation practice
Security-tool experimentation

⚠️ Important: This laboratory must only be used for systems that you own or have explicit permission to test. Do not use the lab or its tools to attack unauthorized systems.


### Requirements

Before starting, ensure that you have the following:


A computer running Windows
Oracle VirtualBox installed
The Kali Linux ISO image or prebuilt VirtualBox virtual machine image

At least 8 GB of RAM recommended, with additional memory providing better performance.

At least 30 – 40 GB of free disk space.

### Setup Procedure
### Step 1: Install VirtualBox

Installed VirtualBox using guided installation instructions.

![image alt](https://github.com/lovemorechamboko/NETWORKWALKS-B084-WK1-CYBERSECURITY-LAB-SETUP/blob/29e5eb14d0a857fd99aad2d06c1faddb6563f874/Screenshot%202026-10-26%20005013.png)

### Step 2: Configure Network Settings

Configured the virtual machine's network adapter according to the purpose of the lab.

After virtual machine installation, a dedicated NAT Network was created in VirtualBox.

### Configuration

Network Name: NATNetwork

IPV4 Prefix: 10.0.0.0/24

DHCP: Enabled

IPv6: Disabled

![image alt](https://github.com/lovemorechamboko/NETWORKWALKS-B084-WK1-CYBERSECURITY-LAB-SETUP/blob/c20d01e493b75761b8b84f271eaf4431d1f72a95/Screenshot%202026-10-26%20005140.png)

A NAT Network was selected because multiple virtual machines connected to the same NAT Network can communicate with one another while also having outbound network connectivity.
This will allow future attacker and target VMs to communicate within the lab.

![image alt](https://github.com/lovemorechamboko/NETWORKWALKS-B084-WK1-CYBERSECURITY-LAB-SETUP/blob/2a3f60e24e5a3c7980ceef4cfceffb5577632f7b/Screenshot%202026-10-26%20005428.png)


### Step 3: Create the Virtual Machine

A pre-installed Kali Linux virtual machine was downloaded from the official Kali Linux website and imported into VirtualBox.

![image alt](https://github.com/lovemorechamboko/NETWORKWALKS-B084-WK1-CYBERSECURITY-LAB-SETUP/blob/e91e78d0e601dbf7352f09b7be52dd8eda1ca35b/Screenshot%202026-10-26%20005327.png)


### Step 5: Start Kali Linux

A Virtual machine was started and Kali Linux default (credentials) username and password was used to get into the sysytem..

![image alt](https://github.com/lovemorechamboko/NETWORKWALKS-B084-WK1-CYBERSECURITY-LAB-SETUP/blob/0c5d6757d5f755b73d00384e20a9195b29b35f51/Screenshot%202026-10-26%20005622.png)


### Step 6: Kali Linux Network Configuration Lab

Kali Linux Network Configuration was checked and configured with consistent IPv4 address.

![image alt](https://github.com/lovemorechamboko/NETWORKWALKS-B084-WK1-CYBERSECURITY-LAB-SETUP/blob/7f755b4c6952baabfa479ef86f64e849777abc5e/Screenshot%202026-10-26%20005854.png)


### Step 6: Virtual Machine Accessing the Internet

A ping scan was done to confirm if the virtual machine can access the internet and it was successful.

![image alt](https://github.com/lovemorechamboko/NETWORKWALKS-B084-WK1-CYBERSECURITY-LAB-SETUP/blob/23b0726399ea4f132b74a04d0ec4ef1034d372cd/Screenshot%202026-10-26%20010025.png)

Internet connectivity was also confirmed using Firefox web browser and its was successful.

![image alt](https://github.com/lovemorechamboko/NETWORKWALKS-B084-WK1-CYBERSECURITY-LAB-SETUP/blob/db8edabce8d9decd859e49e1b123e8681a4b7b44/Screenshot%202026-10-26%20010212.png)


### Step 8: Take Snapshots

Using a VirtualBox snapshots to save known-good configurations before performing experiments. If a configuration becomes unstable or a test damages the virtual system, restore the snapshot instead of rebuilding the environment.

![image alt](https://github.com/lovemorechamboko/NETWORKWALKS-B084-WK1-CYBERSECURITY-LAB-SETUP/blob/609c9371aeaab448622b81026873279aa3151f5c/Screenshot%202026-10-26%20010318.png)


## Conclusion

By installing VirtualBox, deploying Kali Linux, configuring suitable virtual hardware, and creating an isolated network for target machines, you can build a practical cybersecurity lab for hands-on learning. This environment supports repeatable experiments in penetration testing, cybersecurity, and defensive security while reducing the risk of affecting real systems.




# 💡 What I Learned

Through this project, I learned how to create and configure a virtual environment for cybersecurity practice.

The most important concepts I learned include:

### 1. NAT vs NAT Network

A standard NAT configuration and a NAT Network serve different purposes.

A NAT Network allows multiple VMs connected to the same virtual network to communicate with one another while providing network address translation for external connectivity.

This makes it useful for building a multi-machine cybersecurity laboratory.

### 2. Virtual Machine Networking

I learned how VirtualBox virtual network adapters connect virtual machines to different types of networks and how network configuration affects communication between machines.

## 3. Static IP Configuration

I learned how to configure and verify IPv4 addressing, subnet masks, gateways, and DNS settings in Kali Linux.

### 4. VM Snapshots

I learned that a clean snapshot should be created before performing risky or experimental activities in order for you to revert back to your previous settings if anything goes wrong .

This provides a known-good recovery point for future cybersecurity exercises.

### 5. Documentation

I learned that documenting commands, configuration, screenshots, problems, and solutions is an important part of a professional cybersecurity project.

## 🔐 Security & Ethical Use

This laboratory is intended strictly for education purposes only.

### 🔗 Tools & Resources

7-Zip: https://7-zip.org/download.html

VirtualBox: https://virtualbox.org/wiki/Downloads

Kali Linux: https://kali.org/get-kali

### 👤 Author

## Lovemore Chamboko

#### Cybersecurity Professional B084

LinkedIn: https://lnkd.in/p/deGpKXQ6

YouTube: https://youtu.be/ztdeoNycSPo?si=lfO1RHR8eYwpwT0W

### 📌 Project Information

##### Program Name: Cybersecurity at Networkwalks | Week: 01 | Project: Cybersecurity & Pentesting Lab Setup | Repository: GitHub
