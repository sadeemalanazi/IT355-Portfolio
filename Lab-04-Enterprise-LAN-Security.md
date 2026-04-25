# Lab 04: Enterprise LAN Security Assessment

## Name: Sadeem Alanazi
## Course: IT 355   

---

# Part 1: Network Architecture

## Network Topology
![Topology](Topology.png)

---

## MAC Address Table
![MAC Address Table](MAC_Address_Table.png)

**Explanation:**  
The MAC address table shows how a switch maps MAC addresses to specific ports, allowing efficient frame forwarding at Layer 2.

---

## Routing Table
![Routing Table](Routing_Table.png)

**Explanation:**  
The routing table shows how routers determine the path for forwarding packets between networks using destination IP and next-hop addresses.

---

## Connectivity Tests

### Same Network Ping
![Same Network Ping](SameNetworkPing.png)

### Cross Network Ping
![Cross Network Ping](CrossNetworkPing.png)

---

## OSI Layer Mapping

- **Layer 1 (Physical):** Cables and connections  
- **Layer 2 (Data Link):** MAC addresses and switching  
- **Layer 3 (Network):** IP addressing and routing  
- **Layer 4 (Transport):** TCP and UDP  
- **Layer 7 (Application):** HTTP, HTTPS, SSH  

---

# Part 2: Protocol Security

## HTTP vs HTTPS
![HTTP](HTTP_Server_Access.png)  
![HTTPS](HTTPS_Server_Access.png)

**Explanation:**  
HTTP sends data in plain text, while HTTPS uses encryption (TLS) to protect data from interception.

---

## TCP vs UDP

TCP is connection-oriented and provides reliability through a handshake process. UDP is connectionless and faster but less secure and harder to monitor.

---

## SSH Login
![SSH](SSH_Login.png)

**Explanation:**  
SSH provides secure encrypted remote access, unlike Telnet which sends data in plain text.

---

# Part 3: Shellshock Vulnerability

![Shellshock Attempt](Shellshock_Attempt.png)

**Explanation:**  
Shellshock is a vulnerability in Bash that allows attackers to execute commands remotely through CGI scripts.

---

# Part 4: Incident Response

## Attack Path

Attacker → Router2 → Router3 → Web Server → SCADA devices  

---

## Root Cause Analysis

| Vulnerability | Issue | Fix |
|--------------|------|-----|
| Unpatched Software | Shellshock vulnerability | Update systems |
| Network Segmentation | Open access | Firewall / ACL |
| Access Control | Weak restrictions | Least privilege |
| Monitoring | No detection | IDS / logging |

---

## Remediation Plan

A multi-layered approach should be implemented, including patching systems, enforcing network segmentation, enabling monitoring tools, and applying zero trust principles.

---

# Reflection

This lab helped me understand how network architecture and security are connected. I learned how segmentation, routing, and protocols work together to protect systems. The Shellshock simulation showed how vulnerabilities can be exploited, and the incident response helped me understand how to defend against attacks.
