# 🖧 Cisco Packet Tracer Network Simulation Project

## Project Overview
This repository contains a Cisco Packet Tracer project simulating a complex network topology. The project includes various networking components and configurations to demonstrate the setup of a detailed and functional network environment.

## Configuration Details

The following configurations have been implemented in the network topology:

- **Routing Protocols**: RIP, OSPF, EIGRP  
- **Switching Technologies**: EtherChannel, HSRP  
- **Access Control**: VLAN configurations, SSH access  
- **IP Addressing**: Static and dynamic IP addressing (DHCP)  
- **Bandwidth and Delay**: Adjusted for different network scenarios  
- **Network Services**: DNS, Web, Email, and Smart Phone configurations  

## Detailed Implementation Instructions

### Key Points Covered in the Configuration Guide

1. **Device Initialization**:
    - Assigning IP addresses to routers and PCs.
    - Setting up VLANs for segmented network traffic.
2. **Protocol Configuration**:
    - Configuring RIP, OSPF, and EIGRP for dynamic routing.
    - Implementing EtherChannel for link aggregation.
3. **Access and Security**:
    - Setting up SSH for secure remote access.
    - Limiting the SSH access only for one device (Mother of Net Admin).
    - Configuring HSRP for high availability.
    - Implementing security good practices like Black Hole VLANs.
4. **Network Services**:
    - DNS and DHCP configuration.
    - Web and email server setups.
    - Smart Phone integration within the network.
5. **Performance Tuning**:
    - Adjusting bandwidth and delay settings for different network segments.


## Explanations
The topology of this project has been divided into 4 sections and a backbone. Different protocols have been configured in routers like [OSPF](https://www.ietf.org/rfc/rfc2328.txt), [RIP](https://datatracker.ietf.org/doc/html/rfc2453), [EIGRP](https://datatracker.ietf.org/doc/html/rfc7868) and [HSRP](https://datatracker.ietf.org/doc/html/rfc2281). In some routers, protocols have been redistributed. Also layer 2 switches and layer 3 switches were configured to have VLANs and inter-VLAN routing. Devices behind wireless routers in Japan section use NAT protocol, so their IP addresses are private. Some security aspects have been considered, for example defining blackhole VLANs. Also an ACL has been defined to deny accessing printer outside of IUT LAN. There are also some servers for example email server, web server, DHCP server and DNS server, so you can make an account in email server and then try to send an email with devices or make a web page and then send HTTP requests with PCs.  
You can simply check all of the configurations, using ```show ru``` command in each device. Also it may be interesting for you, checking ```show ip route``` to see what is going on in routers and how routing algorithms are working.

## How to Run
Install [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) and then simply open the [netlab_project.pkt](netlab_project.pkt). The whole network is in working condition. You can check it by sending a packet from one system to another or through using the PING command in the Cisco Packet Tracer.




