# NETWORKWALKS-B082-WK1-CYBERSECURITY-LAB-SETUP
Cybersecurity &amp; Ethical Hacking Lab Environment Setup

Building an isolated virtual lab for penetration testing and ethical hacking


## 📌Setting Up a Cybersecurity Lab Environment Using VirtualBox and Kali Linux#
# Introduction

Setting up a cybersecurity lab using Oracle VirtualBox and Kali Linux provides a safe, isolated environment for learning and practicing cybersecurity skills. This lab allows users to explore penetration testing, network security, vulnerability assessment, and ethical hacking without affecting their primary operating system or other devices on the network.

# Requirements

Before starting, ensure that you have the following:


A computer running Windows
Oracle VirtualBox installed.
The Kali Linux ISO image or prebuilt VirtualBox virtual machine image.

At least 8 GB of RAM recommended, with additional memory providing better performance.

At least 30–40 GB of free disk space.

# Setup Procedure
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

A Virtual machine was started and Kali Linux default username and password was used to get into the sysytem.

![image alt](https://github.com/lovemorechamboko/NETWORKWALKS-B084-WK1-CYBERSECURITY-LAB-SETUP/blob/0c5d6757d5f755b73d00384e20a9195b29b35f51/Screenshot%202026-10-26%20005622.png)

### Step 4: 

### Step 5: Start and Update Kali Linux

Start Kali Linux and sign in using the credentials configured during installation or supplied for the downloaded image. Open a terminal and update the package lists and installed packages:

bash
sudo apt update
sudo apt full-upgrade -y


Restart the virtual machine if necessary after updates. Take a snapshot in VirtualBox once the system is configured and working correctly.

### Step 6: Install and Configure Lab Tools

Kali Linux includes many cybersecurity tools for different learning objectives. Depending on your lab requirements, you can explore tools for packet analysis, network discovery, web application testing, and vulnerability assessment.

For example, Wireshark can be used to inspect network traffic, while Nmap can be used to discover hosts and services on authorized lab networks.

### Step 7: Create a Controlled Testing Environment

To practice safely, create a second virtual machine containing an intentionally vulnerable operating system or application, such as a deliberately vulnerable training environment. Connect it to the isolated host-only or internal network and verify that it is not exposed to your normal home, workplace, or public network.

Only scan and test systems that you own or have explicit permission to assess.

### Step 8: Take Snapshots and Test the Lab

Use VirtualBox snapshots to save known-good configurations before performing experiments. If a configuration becomes unstable or a test damages the virtual system, restore the snapshot instead of rebuilding the environment.

Verify that Kali Linux starts correctly, network connectivity behaves as expected, and the target virtual machine is accessible only through the intended lab network.

## Conclusion

By installing VirtualBox, deploying Kali Linux, configuring suitable virtual hardware, and creating an isolated network for target machines, you can build a practical cybersecurity lab for hands-on learning. This environment supports repeatable experiments in penetration testing, network analysis, vulnerability assessment, and defensive security while reducing the risk of affecting real systems.
