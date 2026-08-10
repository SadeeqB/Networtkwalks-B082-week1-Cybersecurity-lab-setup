# Networtkwalks-B082-week1-Cybersecurity-lab-setup: Cybersecurity Lab Setup using Virtual box and Kali Linux OS #

The Purpose of setting “Kali Linux Lab” is to provide a safe practice space. Its main goals are: 
  i.  Hands-on skill building: to set up Kali, explore tools, and run exercises (reconnaissance, vulnerability scanning, password cracking, web app analysis, wireless testing, etc.) without legal or operational risk. 
  ii.  Safe experimentation: All testing happens against intentionally vulnerable systems (e.g. Metasploit VMs or other lab targets) inside an isolated network. This prevents accidental damage to real systems or networks. 
  iii.  Realistic simulation: Labs model can be simple setups or more advanced enterprise-like environments (VLANs, firewalls, SIEM tools, Active Directory, etc.) so I can practice both offensive (red-team) and defensive (blue-team) techniques.

Lab environment details are:
  Host machine specs: kali-linux-2026.2, VirtualBox version 7, Network type: NAT Network, IP range: 10.0.0.0/24

Steps are:
  i.  Download and install Virtual Box on my Laptop, using the link: https://virtualbox .org/wiki/Downloads 
  ii.  Configure the Network settings on my Virtual Box, by setting it NAT Network
  iii.  Download and install the Kali Linux on my Virtual Box, using the link: https://kali.org/get-kali
  iv.  Setting my IP configuration on the Kali Virtual Box to 10.0.0.0/24
  v.   Taking the snapshot of the Virtual Machine

Setting up a Kali Linux lab teaches me some practical cybersecurity fundamentals far more effectively than theory alone. The Common lessons include the following:
i.  Safety, Isolation, and Networking: 
  Isolation is non-negotiable. Bridged networking can accidentally expose your lab VMs (or worse, your host) to your real home/work network. Host-only or internal networks keep everything contained while still letting Kali reach the targets. NAT is usually kept for Kali’s internet access (updates, tool downloads). Many people learn this the hard way after a misconfiguration.
  Networking concepts (adapters, subnets, routing, segmentation) become concrete. You stop treating “the network” as abstract and start understanding why traffic flows (or doesn’t).
  Snapshots are essential. Take a clean snapshot of Kali right after install/update and of targets before experiments. This turns “I broke it” into a 30-second rollback instead of hours of rebuilding.

ii.  Linux and System Fundamentals:
  Kali assumes comfort with the terminal and Linux basics (ls, cd, chmod, package management with apt, file system layout, services, users/permissions). Rushing into tools without this foundation leads to constant friction.
  Resource awareness matters: allocate enough RAM/CPU to Kali (commonly 2–4+ GB and 2 vCPUs depending on host hardware) while leaving headroom for targets. Running multiple VMs quickly reveals host limitations.

In short, building the lab itself is a major learning exercise in virtualization, networking, Linux administration, risk containment, and disciplined practice. The tools become useful only after that foundation is solid.

Author: Mohammmed Sadiq Bandiya
Batch: B082-Cybersecurity-Networkwaks Academy
LinkedIn: https://www.linkedin.com/in/mohammed-sadiq-bandiya-80117017?utm_source=share_via&utm_content=profile&utm_medium=member_android

