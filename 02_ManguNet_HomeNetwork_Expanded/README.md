# ManguNet Home Network Expanded

**Lab Type:** Cisco Packet Tracer Simulation

**Objective:** Expand the original ManguNet home network into a dual-LAN /25 subnet architecture with router-based segmentation, switch port-security, and access point conversion for wireless connectivity.

---

## Topology Overview

![Expanded Topology](ManguNet_HomeNetwork_Expanded.Png)

---

## Network Design

| Feature | Description |
|---|---|
Network Type | Dual-LAN (Home and Guest)
Segmentation Method | /25 subnetting
Routing | Cisco 2911 router providing inter-LAN routing
Security | Sticky MAC address port-security on LAN-A switch
Wireless | WRT300N configured as Access Point (DHCP disabled)

---

## Network Subnets

| LAN | Subnet | Mask | Gateway |
|---|---|---|---|
LAN-A (Home) | 192.168.1.0/25 | 255.255.255.128 | 192.168.1.1
LAN-B (Guest) | 192.168.1.128/25 | 255.255.255.128 | 192.168.1.129

---

## Devices and IP Scheme

### LAN-A (Home Network)

| Device | Hostname | IP Address | Connection |
|---|---|---|---|
Desktop 1 | PC-Jovany | 192.168.1.10 | Wired
Desktop 2 | PC-Family | 192.168.1.11 | Wired
Laptop | Laptop-Loaner | 192.168.1.12 | Wired
Printer | PRN-Home | 192.168.1.13 | Wired
Access Point | AP-ManguNet | 192.168.1.2 | Wired

### LAN-B (Guest Network)

| Device | Hostname | IP Address | Connection |
|---|---|---|---|
Guest Desktop 1 | PC-Guest1 | 192.168.1.130 | Wired
Guest Desktop 2 | PC-Guest2 | 192.168.1.131 | Wired
Printer | PRN-Guest | 192.168.1.132 | Wired

---

## Verification

- LAN-A devices successfully ping each other
- LAN-B devices successfully ping each other
- Routing between LAN-A and LAN-B confirmed
- Access Point reachable, DHCP disabled
- Sticky MAC port-security enforced on LAN-A switch

---

## Lessons Learned

- Subnetting and addressing with /25 masks
- Router configuration for multi-LAN connectivity
- Enforcing Layer-2 security with sticky MAC addresses
- Converting a residential router to AP mode
- Documenting network topology, addressing, and verification steps clearly

---

## Next Steps

- Implement VLANs and trunking to replace physical segmentation
- Add ACLs to control traffic between networks
- Add DHCP services for automated addressing
- Introduce perimeter firewall or virtual security appliance

---

## Related Work

This project is an expansion of the original ManguNet deployment:  
[01_ManguNet_HomeNetwork](../01_ManguNet_HomeNetwork)

---

**Status:** Completed  
**Tools Used:** Cisco Packet Tracer
