# Cybersecurity Lab Setup using Virtual box and Kali Linux OS #

📌 PROJECT OVERVIEW:

This project focuses on setting up a virtual cybersecurity and penetration-testing laboratory using VirtualBox and Kali Linux.
The purpose of the lab is to create a controlled environment where cybersecurity tools, network scanning, reconnaissance, vulnerability assessment, and other security-testing activities can be performed safely and repeatedly.
The lab is configured on a private virtual network so that additional machines can be added later and used as targets for authorized security testing.

🎯 THE MAIN OBJECTIVES OF THIS PROJECT ARE TO:

Install and configure VirtualBox.
Install/import Kali Linux as a virtual machine.
Create a private NAT Network for the cybersecurity lab.
Configure network connectivity for Kali Linux.
Assign a consistent IP address to the Kali VM.
Verify network connectivity and DNS resolution.
Take a clean VM snapshot for recovery.
Document the complete setup process.
Prepare the environment for future cybersecurity projects.

🛡️ THE PURPOSE OF THIS LAB:

The Lab provides an isolated and controlled environment for Cybersecurity learning and authorized security testing.
It can be used for activities such as:
  Network Reconnaissance
  Port Scanning
  Vulnerability Assessment
  Packet Analysis
  Exploitation Practice
  Security-tool Experimentation

Important: This laboratory must only be used for systems that you own or have explicit permission to test. Do not use the lab or its tools to attack unauthorized systems.

🏗️ LAB ARCHITECTURE:

<img width="2600" height="1186" alt="image" src="https://github.com/user-attachments/assets/41db100e-bcf5-489d-b4f2-844fa477e2cd" />


⚙️ LAB CONFIGURATION:

🧩 Component	⚙️ Configuration

🖥️ Host OS	Windows 10

🧠 Host RAM	8 GB

⚡ Processor	Intel Core i5

🧰 Hypervisor	VirtualBox 7.0.20

🐉 Security OS	Kali Linux 2026.2

🧠 Kali RAM	2048 MB

🌐 Virtual Network	NAT Network

📡 Network Address	10.0.0.0/24

🐧 Kali IP Address	10.0.0.2/24

🚪 Default Gateway	10.0.0.1

🌍 DNS Server	8.8.8.8

🔮 Future VM Range	10.0.0.3–10.0.0.99




🪜 LAB SETUP PROCEDURE:

Step 1. Install 7-Zip
7-Zip was installed to extract the Kali Linux virtual-machine package, which may be distributed as a .7z archive.

Tool: 7-Zip

Step 2. Install VirtualBox
VirtualBox was installed as the hypervisor.

Step 3. Create the NAT Network
A dedicated NAT Network was created in VirtualBox.

Configuration: Network Name: NATNetwork IPv4 Prefix: 10.0.0.0/24 DHCP: Enabled IPv6: Disabled

<img width="2874" height="1702" alt="image" src="https://github.com/user-attachments/assets/78f2c769-855d-4c9f-baa0-84efe7a2b6cb" />

A NAT Network was selected because multiple virtual machines connected to the same NAT Network can communicate with one another while also having outbound network connectivity.

This will allow future attacker and target VMs to communicate within the lab.

Step 4: Import Kali Linux
The Kali Linux virtual machine was downloaded from the official Kali Linux website and imported into VirtualBox.

The VM network adapter was configured as follows:

Adapter 1
Attached to: NAT Network
Network:     NatNetwork
Adapter Type: Intel PRO/1000 MT Desktop
The VM was allocated:

RAM: 2048 MB

<img width="1998" height="1166" alt="My Kali Linux Screenshot" src="https://github.com/user-attachments/assets/1cca4008-372c-4801-861b-8783cd92be18" />

A shared folder was also configured for transferring required files between the host operating system and the Kali VM.

Step 5: Configure the Kali Linux Network
The Kali Linux network configuration was checked and configured with a consistent IPv4 address.
Example configuration:
IP Address: 10.0.0.2
Subnet Mask: 255.255.255.0
Gateway: 10.0.0.1
DNS: 8.8.8.8
A consistent IP address makes it easier to document the lab and reference the Kali machine in future exercises.

<img width="1998" height="1166" alt="image" src="https://github.com/user-attachments/assets/766b7b3b-3377-4900-9e4a-0ead5b572268" />

Step 6: Create a Clean VM Snapshot
After completing the initial configuration, a VirtualBox snapshot was created.

Example snapshot name:

Clean Kali - Network Setup
The snapshot represents the clean baseline of the laboratory.

If a future exercise changes or damages the VM configuration, the machine can be restored to this baseline.


Example Results:

IP Address:
10.0.0.2/24

Gateway:
10.0.0.1

DNS:
8.8.8.8

🐞 PROBLEMS ENCOUNTERED & SOLUTIONS:

Documenting problems is an important part of the project.

Problem 1. Internet Connectivity After Static IP Configuration
After manually configuring the IPv4 settings, Internet connectivity may fail depending on the Kali/NetworkManager configuration.

One workaround used during this lab was:

sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0
The network connection was then restarted/rebooted and connectivity was tested again.

Important: Network interface and connection names may differ between systems. Students should first identify their actual connection name before running an nmcli command.

Problem 2. VirtualBox VT-x / Virtualization Error
The VM initially failed to start because hardware virtualization was disabled in the system firmware/BIOS.

The issue was resolved by:

Restarting the computer.
Entering BIOS/UEFI settings.
Enabling Intel VT-x / hardware virtualization.
Saving the configuration.
Restarting the computer.
Starting the Kali VM again.
After enabling virtualization, the VM started successfully.

💡 WHAT I LEARNED:

Through this project, I learned how to create and configure a virtual environment for cybersecurity practice.

The most important concepts I learned include:

1. NAT vs NAT Network
A standard NAT configuration and a NAT Network serve different purposes.

A NAT Network allows multiple VMs connected to the same virtual network to communicate with one another while providing network address translation for external connectivity.

This makes it useful for building a multi-machine cybersecurity laboratory.

2. Virtual Machine Networking
I learned how VirtualBox virtual network adapters connect virtual machines to different types of networks and how network configuration affects communication between machines.

3. Static IP Configuration
I learned how to configure and verify IPv4 addressing, subnet masks, gateways, and DNS settings in Kali Linux.

4. VM Snapshots
I learned that a clean snapshot should be created before performing risky or experimental activities.

This provides a known-good recovery point for future cybersecurity exercises.

5. Documentation
I learned that documenting commands, configuration, screenshots, problems, and solutions is an important part of a professional cybersecurity project.

🔐 SECURITY AND ETHICAL USE:

This laboratory is intended strictly for education purposes only.

🔗 TOOLS AND RESOURCES:

7-Zip: https://7-zip.org/download.html

VirtualBox: https://virtualbox.org/wiki/Downloads

Kali Linux: https://kali.org/get-kali

👤 AUTHOR:

Mohammed Sadiq Bandiya
Cybersecurity- Penetration Testing and Ethical Hacking Intern — Batch B082 - NetworkWalks Academy
LinkedIn: https://www.linkedin.com/in/mohammed-sadiq-bandiya-80117017?utm_source=share_via&utm_content=profile&utm_medium=member_android


📌 PROJECT INFORMATION:

Internship: Cybersecurity - Penetration Testing and Ethical Hacking Internship
Week: 01
Project: Cybersecurity & Pentesting Lab Setup
Organization: NetworkWalks Academy
Repository: GitHub
