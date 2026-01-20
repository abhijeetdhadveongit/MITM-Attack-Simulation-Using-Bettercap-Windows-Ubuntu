MITM Attack Simulation Using Bettercap

## Windows & Ubuntu Environment

## About me 

Author: Abhijeet Dhadve 

Role: Ethical Hacker / Security Analyst

Date: January 2026

Tools: Kali Linux, Bettercap, Wireshark

---

## Table of Contents

1. Executive Summary

2. Objectives

3. Scope & Ethical Considerations

4. Lab Environment & Architecture

5. Methodology

6. Network Reconnaissance

7. MITM Positioning (ARP Spoofing)

8. Traffic Interception & Analysis

9. Credential Exposure Analysis

10. Browser & TLS Security Evaluation

11. Detection & Defensive Analysis

12. Mitigation & Validation

13. Risk Assessment Summary

14. Lessons Learned

15. Conclusion

16. Appendix – Evidence

---

## 1. Executive Summary

This project demonstrates a controlled Man-in-the-Middle (MITM) attack simulation against Windows and Ubuntu systems using Bettercap. The assessment highlights risks associated with flat network architectures, insecure communication protocols, and lack of monitoring. The goal was to analyze attacker capabilities and validate modern defensive controls in an ethical lab environment.


## 2. Objectives

-Simulate MITM attacks using ARP spoofing

-Intercept and analyze network traffic

-Identify credential exposure risks

-Evaluate browser and TLS protections

-Demonstrate detection and mitigation strategies


## 3. Scope & Ethical Considerations

### In Scope

-Kali Linux attacker VM

-Windows 10/11 victim VM

-Ubuntu victim VM

-Internal virtual network

### Out of Scope

-Public or corporate networks

-Real user credentials

-Malware or destructive payloads

### Ethical Statement

All testing was conducted on self-owned systems in a controlled lab environment for educational purposes only.


## 4. Lab Environment & Architecture
Virtual Machines - 

- Attacker - Kali Linux

- Victim 1 - Windows 10/11

- Victim 2 - Ubuntu

- Network - Internal / Host-only

A network diagram is provided in the diagrams folder.


## 5. Methodology

The assessment followed a penetration testing lifecycle:

1.Reconnaissance

2.MITM positioning

3.Traffic interception

4.Credential exposure analysis

5.Detection and mitigation

## 6. Network Reconnaissance

Network discovery was performed using Bettercap to identify live hosts, IP addresses, and MAC mappings within the subnet. Both Windows and Ubuntu systems were successfully enumerated, confirming a flat Layer-2 network architecture.

### Impact:
Flat networks increase susceptibility to MITM attacks.


## 7. MITM Positioning (ARP Spoofing)

ARP spoofing was used to position the attacker between the victim and the default gateway in full-duplex mode. Traffic was transparently relayed, and victim connectivity remained unaffected.

### Impact:
Confidentiality and integrity of network traffic could be compromised.


## 8. Traffic Interception & Analysis

Intercepted traffic analysis revealed cleartext HTTP communication and DNS metadata exposure. HTTPS traffic remained encrypted, validating modern browser protections while highlighting metadata leakage risks.


## 9. Credential Exposure Analysis

Authentication over HTTP resulted in cleartext credential exposure. Encrypted authentication mechanisms such as HTTPS and SSH effectively protected credentials from interception.


## 10. Browser & TLS Security Evaluation


Modern browsers enforced HTTPS and HSTS policies, preventing SSL downgrade attacks. Certificate warnings were observed during attempted manipulation.


## 11. Detection & Defensive Analysis


Indicators of compromise included ARP anomalies, duplicate MAC mappings, and abnormal ARP traffic volumes. Detection using packet analysis was feasible but required active monitoring.


## 12. Mitigation & Validation

### Recommended mitigations included:

-HTTPS + HSTS enforcement

-Network segmentation

-Dynamic ARP Inspection

-IDS/IPS deployment

-Deploy static ARP rule 


## 13. Risk Assessment Summary

### Vulnerability and its Severity

1.ARP Spoofing - High

2.Cleartext Credentials - High

3.Metadata Leakage - Medium

4.Lack of Monitoring - Medium


## 14. Lessons Learned

-OS choice does not mitigate Layer-2 attacks

-Encryption is essential but not sufficient

-Detection is critical for early response

-Defense-in-depth is required

-Static ARP hardening prevented ARP-based traffic redirection; however, passive traffic observation remained possible due to shared Layer-2 virtualization, highlighting the distinction between MITM prevention and network visibility.


## 15. Conclusion

This project demonstrates that MITM attacks remain a serious risk in flat networks. While encryption significantly reduces impact, proper network design and monitoring are essential to prevent and detect such attacks.


## 16. Appendix – Evidence

Evidence screenshots and packet captures are organized by phase in the evidence/ directory.
