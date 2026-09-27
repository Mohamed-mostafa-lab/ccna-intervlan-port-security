Project Overview:
Designed and deployed a highly secure, hierarchical enterprise network topology simulating a Healthcare Environment using Cisco Packet Tracer. The project emphasizes strict network segmentation, access control, and centralized security monitoring, aligning with SOC (Security Operations Center) best practices.

Key Technical Implementations:

Logical Segmentation: Implemented VLANs and Router-on-a-Stick (802.1Q) to isolate Medical Staff, Medical IoT Devices, IT Management, and Guest WiFi traffic.

Security & Access Control (ACLs): Configured Extended Access Control Lists to act as a firewall, explicitly denying Guest and IT subnets from accessing critical Medical IoT infrastructure, while permitting authorized medical staff.

Layer 2 Security: Enforced Port Security (MAC Sticky, Maximum 1, Violation Shutdown) on edge switch ports to mitigate unauthorized physical access risks.

Centralized Logging (SOC): Configured a centralized Syslog Server to aggregate and timestamp security events and configuration changes across network devices for auditing and incident response.

Automated Provisioning: Configured centralized DHCP pools for dynamic IP allocation across all isolated subnets.

Wireless Connectivity: Deployed an autonomous Access Point with WPA2-PSK security to provide isolated internet access for the Guest VLAN.
