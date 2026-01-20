# MITM Attack Simulation Using Bettercap (Windows & Ubuntu)

## Project Overview

This project demonstrates a controlled Man-in-the-Middle (MITM) attack simulation against Windows and Ubuntu systems using Bettercap in an isolated lab environment. The goal is to analyze network-layer attack feasibility, traffic interception risks, credential exposure, and modern defensive mechanisms.

All testing was conducted ethically on self-owned virtual machines.

---

## Objectives

- Simulate MITM attacks using ARP spoofing
- Intercept and analyze network traffic
- Identify cleartext credential exposure risks
- Evaluate HTTPS, TLS, and HSTS protections
- Demonstrate detection and mitigation strategies
- Produce a professional penetration testing report

---

## Lab Environment

Attacker - Kali Linux 

Victim 1 - Windows 11 

Victim 2 - Ubuntu


---

##  Tools Used

- Bettercap
- Wireshark
- tcpdump
- Kali Linux
- VirtualBox / VMware

---

## Project Methodology

1. Network Reconnaissance  
2. MITM Positioning (ARP Spoofing)  
3. Traffic Interception & Analysis  
4. Credential Exposure Analysis  
5. Browser & TLS Security Evaluation  
6. Detection & Defensive Analysis  
7. Mitigation & Risk Assessment  

---

## Key Findings

- Flat networks are highly susceptible to MITM attacks
- Cleartext HTTP authentication exposes credentials instantly
- HTTPS/TLS effectively protects credential confidentiality
- Metadata leakage persists even in encrypted sessions
- Windows and Ubuntu are equally vulnerable at Layer 2
- Lack of monitoring significantly delays attack detection

---

## Mitigations Implemented

- Enforced HTTPS and HSTS
- Network segmentation recommendations
- IDS/IPS detection strategies
- VPN usage for untrusted networks
- ARP anomaly monitoring

---

## Report

The full penetration testing report is available in the `report/` directory and includes:
- Executive summary
- Technical findings
- Risk ratings
- Mitigation recommendations
- Evidence screenshots

---

## Ethical Disclaimer

This project was conducted strictly for educational purposes within a controlled lab environment. No real networks, users, or credentials were targeted.

---

## Author

**ABHIJEET DHADVE**  
Aspiring Penetration Tester / SOC Analyst  
