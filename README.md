# ICMP Network Analysis with tcpdump & hping3

## Overview
This project demonstrates hands-on analysis of Internet Control Message Protocol (ICMP) behavior using packet-crafting and packet-capture tools. The goal was to intentionally trigger different ICMP error messages, capture both stimulus and response traffic, and analyze protocol-level behavior relevant to network troubleshooting, security monitoring, and incident response.

This lab reflects real-world scenarios where ICMP messages are used to diagnose connectivity issues, detect filtering behavior, or identify misconfigurations.

---

## Tools & Technologies
- tcpdump
- hping3
- nmap
- Kali Linux
- Wireshark (for validation)

---

## ICMP Scenarios Analyzed
The following ICMP message types were generated and analyzed:

- **ICMP Port Unreachable (Type 3, Code 3)**
- **ICMP Time-To-Live Exceeded (Type 11, Code 0)**
- **ICMP Admin Prohibited (Type 3, Code 13)**
- **ICMP Protocol Unreachable (Type 3, Code 2)**

Each scenario includes:
- Packet stimulus generation
- tcpdump capture filters
- Hex and ASCII packet inspection
- Protocol field interpretation

Detailed breakdowns are available in the `/analysis` directory.

---

## Methodology
1. Crafted stimulus packets using `hping3` or `nmap`
2. Captured both outbound and inbound packets using `tcpdump`
3. Analyzed ICMP headers, type/code values, and payload references
4. Correlated responses to network behavior and filtering logic

---

## Detection & Defensive Relevance
From a defensive perspective, this project highlights:
- How ICMP messages appear in packet captures and logs
- How firewalls and routers enforce policy using ICMP responses
- How excessive ICMP traffic may indicate scanning or reconnaissance activity

These behaviors are commonly monitored in IDS/IPS systems and SIEM platforms.

---

## Key Takeaways
- ICMP remains critical for network diagnostics and security visibility
- Packet-level inspection provides insight beyond tool-generated output
- Proper filtering and logging of ICMP traffic improves detection capabilities

---

## Disclaimer
All traffic was generated in a controlled lab environment for educational purposes only. No unauthorized scanning or testing was performed.
