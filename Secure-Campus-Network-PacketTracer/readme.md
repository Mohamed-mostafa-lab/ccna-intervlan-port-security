# Secure University Campus Network 🎓🛡️

## Project Overview
This project is a comprehensive simulation of a secure, enterprise-grade University Campus Network built using Cisco Packet Tracer. The architecture focuses on high availability, logical segmentation, and proactive internal threat mitigation, aligning with modern Blue Team and Security Operations Center (SOC) best practices.

## Network Architecture
The network is designed using a modified Three-Tier structure, categorizing traffic into highly controlled zones:
* VLAN 10 (Faculty & Admin): Isolated management and academic staff network.
* VLAN 20 (Students & Labs): High-traffic zone with wireless access. Treated as an untrusted zone for security testing.
* VLAN 30 (DMZ): Houses the public-facing University Web Portal.
* VLAN 40 (Internal Data Center): Highly secured zone hosting the Grades Database and the Centralized Syslog/SOC Server.

## Key Technologies & Protocols Implemented

### 1. Core Networking
* **Router-on-a-Stick (802.1Q):** Facilitates efficient inter-VLAN routing across the campus.
* **LACP EtherChannel:** Aggregated multiple physical links between the Core Switch and Student Access Switch to increase bandwidth and provide link redundancy.
* **Dynamic Host Configuration Protocol (DHCP):** Centralized IP address pools configured on the Core Router for Faculty and Student networks.

### 2. Cybersecurity & Blue Teaming
* **DHCP Snooping:** Configured on access switches to strictly trust only the core uplink, successfully mitigating simulated Rogue DHCP server attacks from a dedicated "Hacker Zone".
* **Extended Access Control Lists (ACLs):** Configured Firewall rules (ACL 101) to block untrusted student subnets from reaching the Internal Data Center, while permitting access to the DMZ.
* **Centralized SOC Logging:** Configured network devices to forward timestamped system logs and security events to a centralized Syslog server for real-time monitoring and incident response.

## Repository Contents
* `Secure_Campus_Network.pkt` - The main Cisco Packet Tracer simulation file.
* `Screenshots/` - Directory containing visual proof of topology, successful EtherChannel formation, ACL blocks, and Syslog event captures.

## How to Run
1. Download and install [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer).
2. Open the `Secure_Campus_Network.pkt` file.
3. Access the `Campus-Router` or `Student-Switch` CLI to review the `running-config`.
4. Test the ACLs by attempting to ping the Grades Database (`192.168.40.100`) from the Student PC (Should result in Destination Unreachable).
