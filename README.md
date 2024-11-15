# Networking Fundamentals for Cybersecurity

This is formatted to offer both a technical and practical study guide

## Table of Contents
- [1. Networking Basics](#1-networking-basics)
  - [IP Addressing](#ip-addressing)
  - [MAC Addresses](#mac-addresses)
  - [Ports and Protocols](#ports-and-protocols)
- [2. OSI and TCP/IP Models](#2-osi-and-tcpip-models)
  - [OSI Model](#osi-model)
  - [TCP/IP Model](#tcpip-model)
- [3. Routing and Switching](#3-routing-and-switching)
  - [Routing](#routing)
  - [Switching](#switching)
- [4. Network Security Fundamentals](#4-network-security-fundamentals)
  - [Firewalls and Access Control](#firewalls-and-access-control)
  - [NAT (Network Address Translation)](#nat-network-address-translation)
  - [VPNs and Encryption](#vpns-and-encryption)
- [5. Tools and Protocol Analysis](#5-tools-and-protocol-analysis)
  - [Packet Sniffing](#packet-sniffing)
  - [Network Scanning](#network-scanning)
- [6. Network Attacks and Defense](#6-network-attacks-and-defense)
  - [Common Attack Types](#common-attack-types)
  - [Detection and Prevention](#detection-and-prevention)

---

### 1. Networking Basics
- #### IP Addressing
   Understand IPv4 and IPv6, including subnetting and CIDR notation.
  - ##### IPv4
    Consists of 32-bit addresses, divided into four 8-bit sections separated by periods (e.g., 192.168.1.1).
    This format supports around 4.3 billion addresses.
  - ##### IPv6
    Uses 128-bit addresses to allow more devices. They look much longer (e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334).
  - ##### Subnetting
    Splits IP networks into smaller sections, allowing efficient allocation of addresses. For example, 192.168.1.0/24
    is a subnet that divides the IP space into chunks of 256 addresses.
  - ##### CIDR Notation
    Represents IP ranges compactly (e.g., 192.168.1.0/24 shows a block where 24 bits are fixed, and the remaining bits
    are for device addresses).
  - ##### Testing:
    Ping: using the ping command in terminal to test connectivity to an IP address, like ping 8.8.8.8 (Google DNS). It will show data packets being sent and received.

    Traceroute: Run tracert [IP address] (on Windows) or traceroute [IP address] (on macOS/Linux) to see the path data      takes across networks to reach a target IP.

- #### MAC Addresses
   Know how devices are uniquely identified at the hardware level within local networks. Operates at a Layer 2
   (Data Link) of the OSI model, which manages local network communication. A MAC address typically looks like
   00:1A:2B:3C:4B:5E.

   They are critical in switching environments because switches use them to direct data to the correct device within a network
   Unlike IP addresses, MAC addresses don't change. They're assigned by the device's manufacturer and are permanently associated with that piece of hardware.
  - ##### Testing:
    Find MAC Address: Use the command ipconfig /all on Windows or ifconfig /ip link on macOS/Linux to view the view the MAC addresses of your network interfaces.

    ARP (Address Resolution Protocol): Try using arp -a to see a table of IP addresses and their associated MAC addresses in your local network, showing how devices communicate at both the IP and MAC levels.

- #### Ports and Protocols
   Common protocols (e.g., HTTP, HTTPS, FTP, SSH, DNS, etc.), their associated ports, and how they're used.
  - ##### Protocols
    Protocols define the rules and conventions for data exchange between devices, specifying things like how data
    is formatted, how errors are detected and corrected, and how connections are managed. Some common protocols include:
    * HTTP (Hypertext Transfer Protocol) - Port 80: For web traffic.
    * HTTPS (HTTP Secure) - Port 443: For encrypted web traffic.
    * FTP (File Transfer Protocol) - Ports 20/21: Used for filetransfers.
    * DNS (Domain Name System) - Port 53: Converts human-readable domain names into IP addresses.
    * SSH (Secure Shell) - Port 22: Allows secure remote access to devices.
    * SMTP (Simple Mail Transfer Protocol) - Port 25: For email sending.
  - ##### Ports
    Ports are numbered endpoints (0-65535) on devices that receive and send data associated with a protocol. These are divided into:
    * Well-Known Ports (0-1023): Reserved for standard protocols like HTTP (80), FTP (21), etc
    * Registered Ports (1024-49151): Used by comapnies for proprietary applications.
    * Dynamic or Private Ports (49152-65535): Used by client applications to initiate connections (e.g., web browsers).
  - ##### TCP and UDP
    Two main types of communication:
    * TCP (Transmission Control Protocol): Ensures reliable, ordered data delivery. Good for applications where data integrity is crucial, like web browsing and email.
    * UDP (User Datagram Protocol): Focuses on speed over reliability, commonly used for streaming and gaming where a few dropped packets don't impact the overall experience.
  - ##### Testing
    Open Ports:
    * Port Scanning: Use tools like nmap to discover open ports on a device. Running nmap [IP address] will show which ports are open and which protocols are in use.

    Protocols in Action:
    * Wireshark: Capture packets on your network to see protocols like HTTP, DNS, and FTP in real-time. Look for source and destination IPs, ports, and observe protocol-specific behavior (e.g., HTTP GET requests or DNS queries).

    Testing Connections:
    * Telnet: Open a terminal and use telnet [IP address] [port] to test whether a port is open and receiving connections. 
    

### 2. OSI and TCP/IP Models
- #### OSI Model
   Familiarize yourself with the seven layers (Physical, Data Link, Network, Transport, Session, Presentation, Application), which provide a framework for understanding how data moves across networks.

- #### TCP/IP Model
   Focus on the four layers (Link, Internet, Transport, and Application) more directly used in modern networking.

### 3. Routing and Switching
- #### Routing
   Learn how routers manage traffic across networks, including routing protocols (e.g., BGP, OSPF).

- #### Switching
   Understand how switches operate within local networks and how they differ from routers, including VLANs and network segmentation.

### 4. Network Security Fundamentals
- #### Firewalls and Access Control
   Explore how firewalls, both hardware and software, control traffic based on security rules.

- #### NAT (Network Address Translation)
   Learn how NAT hides internal IP addresses for security and network management.

- #### VPNs and Encryption
   Look into secure ways to connect remote users and encrypt data in transit.

### 5. Tools and Protocol Analysis
- #### Packet Sniffing
   Use tools like Wireshark to capture and analyze network traffic.

- #### Network Scanning
   Familiarize yourself with tools like Nmap to map out networks, identify devices, and check for open ports.

### 6. Network Attacks and Defense
- #### Common Attack Types
   Understand attacks such as DDoS, MITM, spoofing, and ARP poisoning.

- #### Detection and Prevention
   Learn how intrusion detection/prevention systems (IDS/IPS) work and how they monitor network traffic for suspicious activity.

---
