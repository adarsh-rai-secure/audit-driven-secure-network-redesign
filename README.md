# Audit-Driven Enterprise Network Security Redesign

This project simulates a real-world engagement as security engineers tasked with rebuilding an indefensible enterprise network for an industrial manufacturer. The company had failed to describe its architecture to external auditors and operated internal systems on public IP space. With a $65,000 budget, we redesigned the network to be segmented, auditable, and resilient.

The redesign introduced clear security boundaries. Internal systems were migrated to RFC1918 space with strict NAT enforcement. Business units were separated into VLANs, with inter-VLAN routing controlled through ACLs and next-generation firewall rules. A multihomed firewall created logical security zones: trusted internal, DMZ, and untrusted Internet edge. Public-facing services were isolated, while Active Directory, DHCP, and internal databases were secured behind controlled access paths.

We implemented 802.1x port-based authentication with RADIUS, port security with MAC limits, and static addressing for critical management and database VLANs. OT systems were isolated into dedicated segments with restricted routing, intrusion detection for industrial protocols, and jump-server-only remote access. Network management workstations were hardened and separated from standard user segments to reduce privilege abuse and lateral movement risk.

Beyond architecture, this was a risk and governance exercise. Every hardware addition was priced, justified, and kept under budget. Firewall rules, NAT tables, DHCP scopes, DNS architecture, ACL policies, and GPO hardening were documented for audit defensibility. The result is a secure, segmented, and monitorable network that aligns technical controls with business risk reduction.
