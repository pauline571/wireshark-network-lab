# Network Security Lab – Wireshark Analysis

## Table of Contents
- [ Overview](#-overview)
- [ Objectives](#-objectives)
- [ Requirements](#-requirements)
- [ Steps](#-steps)
- [ Results](#-results)
- [ Analysis](#-analysis)
- [ Conclusion](#-conclusion)

---

##  Overview
This repository contains practical lab exercises for network security analysis using **Wireshark**. The goal is to capture and analyze network traffic, identify different protocols, and understand the importance of encryption in protecting sensitive information.

##  Objectives
- Capture network traffic with Wireshark.  
- Identify protocols such as **TCP, DNS, HTTP, and TLS**.  
- Observe the TLS handshake process.  
- Understand the role of encryption in secure communications.  
- Evaluate risks associated with unencrypted traffic.  

##  Requirements
- **Wireshark** installed (latest version recommended).  
- Active internet connection to generate traffic.  
- Web browser to visit websites and produce packets.  

##  Steps
1. **Start Capture**: Select the active network interface (Wi-Fi or Ethernet) and begin capturing.  
2. **Generate Traffic**: Visit websites to produce DNS, HTTP, and HTTPS packets.  
3. **Stop Capture**: End the capture after sufficient traffic has been recorded.  
4. **Analyze Packets**: Apply filters (`dns`, `http`, `tls`) to isolate and study specific protocols.  

##  Results
- **Number of packets captured**: **22,922**.  
- **Observed protocols**: TCP, TLSv1.2, DNS, HTTP.  
- **Examples**:  
  - DNS query for `clients1.google.com` resolved to IP `172.217.23.206`.  
  - TLS handshake observed with *Client Hello*, *Server Hello*, and *Certificate*.  
  - HTTP packets visible in clear text.  

##  Analysis
- **Importance of Encryption**: TLS/HTTPS ensures confidentiality and integrity, protecting sensitive data such as passwords and personal information.  
- **Risks of Unencrypted Traffic**: DNS and HTTP traffic can expose visited websites, URLs, and even login credentials in clear text.  

##  Conclusion
This lab demonstrates the difference between encrypted and unencrypted traffic. Encryption is essential for secure communication and user privacy. Wireshark provides a powerful way to visualize these concepts and reinforces the importance of strong authentication and encryption in cybersecurity.
