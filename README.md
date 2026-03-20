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

Results and Analysis


  1.  Approximately how many packets were captured?
Around 17229 packets were captured during the experiment. This shows a significant amount of network activity across different protocols.

2.List three protocols observed during the experiment.
•	DNS → used for resolving domain names (e.g., queries for google.com).
•	HTTP → unencrypted web traffic, visible in clear text (e.g., GET /connecttest.txt).
•	TLS/HTTPS → encrypted communication ensuring confidentiality (e.g., TLS handshake with Client Hello, Server Hello).
(Additionally, TCP was observed as the transport layer establishing reliable connections, and QUIC appeared in the TLS/UDP capture.)

3.Why is encryption important when browsing the internet?
•	Encryption ensures that sensitive information (passwords, personal data, browsing activity) cannot be read by attackers.
•	It protects confidentiality and integrity, preventing interception or modification of data.
•	Without encryption, traffic is exposed in clear text, making users vulnerable to surveillance and attacks.

4.What type of information could attackers obtain from unencrypted traffic?
•	Visited websites and URLs (from DNS and HTTP requests).
•	Login credentials or personal data if sent via HTTP.
•	Files or messages transmitted without protection.
•	Essentially, attackers can reconstruct a user’s browsing activity and intercept sensitive information.



