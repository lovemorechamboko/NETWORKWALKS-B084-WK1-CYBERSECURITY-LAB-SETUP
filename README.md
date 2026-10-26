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

Download Oracle VirtualBox from the official website at https://www.virtualbox.org/. Install the version compatible with your operating system, following the installation instructions provided.

![image alt](https://github.com/lovemorechamboko/NETWORKWALKS-B084-WK1-CYBERSECURITY-LAB-SETUP/blob/29e5eb14d0a857fd99aad2d06c1faddb6563f874/Screenshot%202026-10-26%20005013.png)

### Step 2: Configure Network Settings

Configured the virtual machine's network adapter according to the purpose of the lab.

After virtual machine installation, a dedicated NAT Network was created in VirtualBox.

Configuration
Network Name: NATNetwork
IPV4 Prefix: 10.0.0.0/24
DHCP: Enabled
IPv6: Disabled


A NAT Network was selected because multiple virtual machines connected to the same NAT Network can communicate with one another while also having outbound network connectivity.
This will allow future attacker and target VMs to communicate within the lab.


Download Kali Linux

Visit the official Kali Linux website at https://www.kali.org/get-kali/. Download either the installer ISO image or the prebuilt VirtualBox image. Using the prebuilt VirtualBox image can simplify the setup process because the virtual machine is already configured.

### Step 3: Create the Virtual Machine

If you downloaded the ISO image, open VirtualBox and select New. Name the virtual machine “Kali Linux,” select the appropriate Linux operating system type, and allocate suitable resources.

A reasonable starting configuration is:

Memory: 4 GB RAM.
Processors: 2 CPU cores.
Virtual hard disk: 40 GB, dynamically allocated.

Attach the downloaded Kali Linux ISO to the virtual optical drive. Start the virtual machine and follow the installation wizard to install Kali Linux on the virtual disk.

If you downloaded the prebuilt VirtualBox image, extract the archive and import the provided virtual machine appliance or open the supplied virtual machine configuration file, as applicable.

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
