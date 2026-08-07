Cisco Enterprise Network Security Lab

Overview

This project demonstrates the design and implementation of a small enterprise branch-office network using Cisco Packet Tracer.

The lab focuses on network segmentation, controlled communication between departments, access-control enforcement, and secure administrative access.

The security design uses:

VLAN Segmentation → Inter-VLAN Routing → ACLs → SSH

⸻

Network Scope

The simulated enterprise network contains:

* 1 Cisco 2960 switch
* 1 Cisco 1941 router
* 8 PCs
* 3 VLANs
* 3 departmental network segments

Departments

Department	Network Segment
Administration	Admin VLAN
Sales	Sales VLAN
IT Support	IT VLAN

⸻

Network Architecture

                         Cisco 1941 Router
                                |
                         802.1Q Trunk
                                |
                                |
                      Cisco 2960 Switch
                    /         |         \
                   /          |          \
                  ▼           ▼           ▼
             Admin VLAN   Sales VLAN   IT VLAN
                 |            |            |
              PCs            PCs          PCs

⸻

1. VLAN Segmentation

The network was divided into three VLANs to separate departmental traffic.

Administration VLAN

Used for administrative functions such as HR and Finance.

Sales VLAN

Used to isolate sales-related systems and traffic.

IT Support VLAN

Used for IT-support systems and administrative activities.

VLAN segmentation reduces the need for all systems to operate within the same broadcast domain and provides a foundation for applying security policies between departments.

⸻

2. Inter-VLAN Routing

Inter-VLAN communication was implemented using the Cisco router.

The switch-to-router connection used 802.1Q trunking, allowing multiple VLANs to traverse the same physical link.

Admin VLAN ──┐
             │
Sales VLAN ──┼── 802.1Q Trunk ── Router
             │
IT VLAN ─────┘

This provided controlled communication between the departmental networks.

⸻

3. Access Control Lists

Access Control Lists (ACLs) were implemented to control communication between network segments.

The security objective was to prevent unrestricted communication while allowing approved traffic between departments where required.

This demonstrates the principle of:

Allow only the communication that is required.

ACLs therefore served as a network-layer access-control mechanism supporting least-privilege principles.

⸻

4. Secure Device Administration

SSH was configured for remote administration of the network devices.

This provided a more secure administrative mechanism than unencrypted remote-management protocols.

The lab therefore demonstrates the relationship between:

Network Access → Authentication → Secure Administration

⸻

5. Security Design

The security architecture can be summarized as:

                 Enterprise Network
                         |
                         ▼
                  VLAN Segmentation
                         |
                         ▼
                 Inter-VLAN Routing
                         |
                         ▼
                       ACLs
                         |
                         ▼
                 Controlled Traffic
                         |
                         ▼
                   SSH Management

Each layer contributes to reducing unnecessary network exposure.

⸻

Quantified Lab Scope

Component	Quantity
Cisco 2960 Switch	1
Cisco 1941 Router	1
PCs	8
VLANs	3
Departments	3

⸻

Skills Demonstrated

Networking

* Cisco Packet Tracer
* VLANs
* 802.1Q trunking
* Inter-VLAN routing
* Routing and switching
* IP addressing

Network Security

* Access Control Lists
* Network segmentation
* Least-privilege communication
* Secure administrative access
* SSH

Security Architecture

* Departmental isolation
* Controlled east-west traffic
* Access-control enforcement
* Defense-in-depth concepts

⸻

Security Objectives

The lab was designed to demonstrate:

Segmentation

Separate departments into distinct network segments.

Access Control

Restrict communication between departments using ACL policies.

Secure Administration

Use SSH for remote device management.

Controlled Connectivity

Allow required communication while limiting unnecessary network access.

⸻

Evidence

Recommended evidence structure:

evidence/
├── network-topology.png
├── vlan-configuration.png
├── trunk-configuration.png
├── inter-vlan-routing.png
├── acl-configuration.png
└── ssh-configuration.png

Before publishing screenshots, remove or obscure:

* Real passwords
* Private credentials
* Unnecessary personal information
* Any real organizational network information

⸻

Lessons Learned

This project reinforced how network architecture and security controls work together.

Segmentation provides separation, routing provides controlled connectivity, ACLs enforce communication policy, and SSH protects administrative access.

Together, these controls create a more defensible enterprise network than relying on a single security mechanism.

⸻

Disclaimer

This project was completed in a controlled educational environment using Cisco Packet Tracer.

It does not represent a production enterprise network.

⸻

Author

Nwanneka James

Cybersecurity | Network Security | SOC Operations | Cloud Security

📧 nwanneka.james@yahoo.com
💼 linkedin.com/in/nwanneka-james
