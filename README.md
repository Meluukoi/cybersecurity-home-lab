# cybersecurity-home-lab
Hands-on cybersecurity home lab using Splunk, Sysmon, Wireshark, Kali Linux, Ubuntu, and VirtualBox.
# Cybersecurity Home Lab Portfolio

## Overview

This repository documents the cybersecurity home lab environment I built to gain real hands-on experience beyond certifications.

After completing the Google Cybersecurity Professional Certificate and CompTIA Security+, I wanted to move from theory into practical cybersecurity work involving:

* Virtualization
* Linux administration
* Network analysis
* SIEM monitoring
* Endpoint telemetry
* Threat investigation
* Security operations workflows

This lab was built entirely on my personal computer using virtual machines and enterprise security tools.

---

# 🔧 Lab Environment

## Host Machine

* Windows 11
* Splunk Enterprise
* Sysmon
* Wireshark

---

## Virtualization Platform

* Oracle VirtualBox

---

## Virtual Machines

### Ubuntu VM

Purpose:

* Linux administration
* Network analysis
* Target machine
* Service hosting

Tools installed:

* Wireshark
* Apache2
* OpenSSH Server

Skills practiced:

* Linux command line
* Package management
* Network troubleshooting
* Port/service auditing
* Packet capture analysis

---

### Kali Linux VM

Purpose:

* Offensive security testing
* Reconnaissance
* Network scanning

Tools used:

* Nmap
* Linux networking tools

Skills practiced:

* Host discovery
* Service enumeration
* Port scanning
* Network reconnaissance

---

# 📡 Networking & Packet Analysis

## Wireshark Analysis

Captured and analyzed:

* ICMP traffic
* DNS requests
* TCP handshakes
* ARP traffic
* NTP traffic
* Nmap scan activity

Concepts learned:

* TCP/IP networking
* TCP three-way handshake
* DNS resolution
* Layer 2 vs Layer 3 traffic
* Network visibility
* Packet filtering
* Protocol analysis

Example filters used:

```bash
icmp
dns
tcp
arp
```

---

# Nmap Reconnaissance

Performed reconnaissance from Kali Linux against the Ubuntu VM.

Commands used:

```bash
nmap <target-ip>
nmap -sV <target-ip>
nmap --script vuln <target-ip>
```

Concepts learned:

* Port scanning
* Service detection
* Attack surface analysis
* Vulnerability enumeration
* Network exposure assessment

---

# Windows Security Monitoring

## Process Analysis

Used PowerShell to investigate:

```powershell
Get-Process | Sort-Object CPU -Descending
```

Skills learned:

* Process monitoring
* Resource analysis
* Windows internals
* Baseline system behavior

---

## Startup Persistence Analysis

Investigated startup applications using:

```powershell
Get-CimInstance Win32_StartupCommand
```

Learned about:

* Persistence mechanisms
* Startup entries
* Endpoint hygiene
* Application behavior

---

## Network Connection Analysis

Commands used:

```powershell
netstat -ano
Get-NetTCPConnection
```

Skills learned:

* Open port analysis
* Listening services
* Network exposure
* Process-to-network correlation

---

# SIEM & Log Analysis

## Splunk Enterprise

Installed and configured Splunk Enterprise on Windows.

Configured ingestion for:

* Windows Event Logs
* Security logs
* Sysmon telemetry

---

## Splunk Searches

Example searches:

### Failed Logins

```spl
EventCode=4625
```

### Successful Logins

```spl
EventCode=4624
```

### Process Creation Events

```spl
EventCode=1
```

### Network Connections

```spl
EventCode=3
```

### Top Executed Processes

```spl
EventCode=1 | top Image
```

---

# Sysmon Endpoint Telemetry

Installed Sysmon with Sysmon configuration for advanced endpoint visibility.

Monitored:

* Process creation
* Network connections
* File creation
* PowerShell activity
* Parent/child processes

Important Event IDs:

| Event ID | Description        |
| -------- | ------------------ |
| 1        | Process Creation   |
| 3        | Network Connection |
| 11       | File Creation      |

---

# Security Investigations Performed

## Nmap Scan Investigation

* Ran Nmap scans from Kali Linux
* Observed packets in Wireshark
* Investigated telemetry in Splunk
* Correlated timestamps and events

---

## Failed Login Analysis

* Generated failed Windows login attempts
* Investigated Security Event IDs
* Built Splunk searches for authentication events

---

## Endpoint Activity Monitoring

Generated activity by:

* Launching PowerShell
* Opening applications
* Browsing websites
* Running commands

Then investigated:

* Process creation logs
* Network connections
* Event timelines
* Endpoint telemetry

---

# Technical Skills Developed

## Operating Systems

* Windows
* Ubuntu Linux
* Kali Linux

---

## Cybersecurity Tools

* Splunk Enterprise
* Sysmon
* Wireshark
* Nmap
* VirtualBox

---

## Networking

* TCP/IP
* DNS
* ARP
* ICMP
* TCP Handshakes
* Port Analysis
* Service Enumeration

---

## SIEM & Detection

* Splunk SPL queries
* Event investigation
* Log analysis
* Windows Event IDs
* Endpoint telemetry
* Detection thinking

---

## Linux Skills

* Package management
* Service management
* Terminal navigation
* Network troubleshooting
* System auditing

---

# Key Takeaways

This lab helped me move beyond certifications and develop practical cybersecurity skills, including:

* Building virtualized environments
* Troubleshooting systems
* Monitoring endpoint activity
* Performing network analysis
* Investigating logs
* Understanding attacker behavior
* Thinking like a SOC analyst

---


# Contact


Feel free to connect with me or review my projects.


