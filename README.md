SafariTech Solutions — Enterprise Network Lab

Overview

This lab models **SafariTech's HQ network**: a small enterprise topology with clear separation of duties (Engineering vs Sales), a Layer‑3 core switch performing inter‑VLAN routing (SVIs), trunked access switches, and external router links to simulate upstream/ISP connectivity.

It intentionally goes beyond a classroom exercise — the configuration is written as if this were a real deployment: secure management, authenticated routing, useful documentation, and verifiable tests. Think of it as a short, demonstrable portfolio piece for a networking engineer role.


Topology (at a glance)


Core: 3560 L3 Core Switch (SVIs, OSPF area 0, management, hardened)

Access: Two 2960 access switches (Engineering & Sales)

Router: Edge router simulating ISP links and participating in OSPF

Departments & subnets:

Engineering (VLAN 10) — 10.10.10.0/24 — SVI 10.10.10.1

Sales (VLAN 20) — 20.10.10.0/24 — SVI 20.10.10.1

Trunk links between Core ↔ Access (802.1Q), access ports to end hosts


What I built (features & rationale)


**VLAN segmentation & SVIs** — isolates broadcast domains and places inter‑VLAN routing on the L3 core for performance and manageability.

**Trunking** — 802.1Q trunks on distribution links to carry multiple VLANs cleanly.

**OSPF routing** — area 0 used for core routing; simple, industry‑typical design.

**OSPF MD5 authentication** — demonstrates secure routing protocol practice (protects against rogue routers and accidental adjacency).

**SSH v2 + local user auth** — secure out‑of‑band management; service password-encryption to avoid plain text on the console.

**Device hardening** — MOTD banner, exec-timeout, disabled unused ports, descriptive interface naming.

**Documentation-friendly configs** — commented CLI blocks, consistent naming, and verification commands to make the configuration hireable and maintainable.


Networking Keypoints 


Design decision: "I chose SVIs on the L3 switch rather than ROAS for lower latency and higher throughput at the distribution layer."

Security posture: "I used MD5 for OSPF authentication and SSH-only vty access to harden management paths."

Operational readiness: "Configs include interface descriptions, banners, and basic hardening to reflect a production mindset."

Troubleshooting readiness: "I validated connectivity and built verification steps so issues can be triaged quickly."


🌟 Skills Showcased

Advanced Cisco IOS configuration (routing, switching, security)

Subnetting & IP design for enterprise-grade networks

Secure network deployment with industry best practices

Troubleshooting and verification (ping, traceroute, show commands)

Strong pragmatism and creativity in handling complex topologies


🚀 Why This Project Matters

This topology is more than a lab – it reflects my ability to design, configure, and secure enterprise-class networks. It proves my readiness for roles in network engineering, infrastructure design, and network security.

🏆 Author

Bradley Giovanni

Networking Enthusiast |Networking Engineer | Passionate about building secure, scalable networks

EMAIL: giovanniibradley@gmail.com


 [![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/bradley-giovanniii293) 
