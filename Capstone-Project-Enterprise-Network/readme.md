Just successfully completed a comprehensive Enterprise Network Capstone Project on Cisco Packet Tracer! 🚀

This lab wasn't just about dragging and dropping devices; it was a deep dive into building a robust, hybrid infrastructure spanning two different sites and overcoming real-world configuration challenges.

Here are the key implementations and technical milestones from this project:
🔹 Infrastructure & Routing: Designed an HQ-to-Branch topology using Router-on-a-Stick for VLAN segmentation. Implemented OSPFv2 for the IPv4 HQ network and OSPFv3 for the IPv6-only Branch network, successfully establishing cross-site connectivity.
🔹 Wireless Management: Configured a Cisco WLC 3504 to broadcast a WPA2-PSK secured Management WLAN via a LAP-PT.
🔹 The Troubleshooting Challenge: The most exciting part was resolving a wireless connectivity issue. The AP wouldn't broadcast the network until I drilled down into the WLC Advanced settings to enable FlexConnect Local Switching and Local Auth, ensuring traffic could be switched locally without dropping, alongside fixing the switchport trunking state.
🔹 Security & Monitoring: Secured the infrastructure using SSH and encrypted passwords. Crucially, I centralized logging by configuring the routers to forward timestamped logs to a central Syslog and NTP Server, a fundamental step for any future SOC operations.

This project reinforced my belief that strong foundational knowledge in Network Architecture and hands-on Troubleshooting are absolutely vital for anyone pursuing a career in Cybersecurity. 🛡️💻
