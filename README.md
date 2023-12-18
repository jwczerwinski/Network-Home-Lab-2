<h1>Network Home Lab 2</h1>

<h2>Overall Description</h2>
Simulate enterprise network in Cisco Packet Tracer with various devices such as PCs, switches, routers, firewalls, and servers. Configuration of a three-tier network model, comprising access, distribution, and core layers; as well as a data center and DMZ. 
<br />
<br />
1. Access layer will provide end-users with network access. Key configurations for the access layer include switches with VLANs, IP addresses and trunk ports, SVIs, NTP and syslog configurations, static routes, and passwords. PC configurations involve static IP addresses and default gateways. 
<br />
<br />
2. Distribution layer will provide aggregation of routing and VLANs to facilitate efficient network performance. Key configurations for distribution layer switches include VLANs, IP addresses, trunk ports, SVIs, OSPF, VRRP, NTP, DHCP relay, DNS, RADIUS, and Syslog. 
<br />
<br />
3. Core layer will provide the high-speed backbone of the network, facilitating data transfer between distribution layer devices and ensuring efficient connectivity across the entire infrastructure. Core layer switches key configurations will include IP addresses, OSPF, NTP, DHCP relay, DNS, RADIUS, and Syslog. 
<br />
<br />
4. The Cisco Adaptive Security Appliance (ASA) configurations will include  interface settings, logging, static routes, object and object group, management protocol settings, OSPF, zone setup, ACLs, NTP and RADIUS, and application inspection. The configuration aims to provide traffic filtering and inspection services for the network and data center, connecting them to an edge router. 
<br />
<br />
5. The data center network switch configurations will include point-to-point layer3 links, OSPF, access ports in VLAN50, etherchannel, NTP, Syslog trap sending, and RADIUS authentication. The data center server configurations will include SSH, as well as services of DNS, NTP, DHCP, RADIUS, and Syslog.
<br />
<br />
6. The edge router configurations will include NAT within the ISP assigned corporate address pool, BGP, DHCP relay, DNS, NTP, Syslog and SSH. The ISP router configurations will include BGP, PAT / NAT, DNS, Syslog and SSH.
<br />
<br />
7. The DMZ ASA configurations will include security levels, authentication, objects and object groups, ACLs and application inspection. The edge router and switch configurations will include static routes, DNS, NTP, Web, Syslog, and SSH.

<h2>Environments Used </h2>

- <b>Cisco Packet Tracer</b> (2.2.43) <br />

- <b>L2 Switch: Cisco IOS C2960 Software Version 15.0(2)SE4</b>  <br />

- <b>ML Switch: Cisco IOS Denali Catalyst L3 Switch (3650), Software Version 16.3.2</b> <br />

- <b>ASA: Cisco Adaptive Security Appliance (5560), Software Version 9.6 </b> <br />

- <b>Router: Cisco IOS C2900 Software, Version 15.1(4)M5</b>  <br />

<h2>Diagram </h2>
<img src="https://i.imgur.com/avTa2kJ.png" height="80%" width="80%" />

<h2>Walk-through:</h2>
<p align="center">
 
[Download Cisco Packet Tracer](https://skillsforall.com/resources/lab-downloads?courseLang=en-US 
)<br />

<br />
<br />
Drag and drop devices as seen in the diagram. Connect devices with appropriate cabling. Label interfaces: <br/>
<img src="https://i.imgur.com/Fu9iR6x.png" height="80%" width="80%" />
<h3> 1. Access Layer </h3>
<h4>  A. PCs </h4>
Static IP addresses, default gateways and DNS server for PCs 1 & 4 for testing. (Setting up DHCP service later)
<img src="https://i.imgur.com/9CYG2OR.png" height="80%" width="80%" />
<h4> B. Access Switches </h4>
Hostname, username, passwords<br />
Switch(config)#hostname SW1<br />
SW1(config)#enable secret password<br />
SW1(config)#username jon secret password<br />
<br />
Vlans, vlan interfaces, trunk and access ports, unused interfaces native vlans, IP addresses
Mgmt interface. Secure unused interfaces. <br />
SW1(config)#vlan 10<br />
SW1(config-vlan)#vlan 11<br />
SW1(config-vlan)#vlan 20<br />
SW1(config-vlan)#vlan 21<br />
SW1(config-vlan)#vlan 100<br />
SW1(config-vlan)#vlan 999<br />
SW1(config-vlan)#exit<br />
<br />
SW1(config-if)#int f0/1<br />
SW1(config-if)#switchport trunk allowed vlan 10,11,20,21<br />
SW1(config-if)#switchport trunk native vlan 999<br />
<br />
SW1(config-if)#int f0/2<br />
SW1(config-if)#switchport trunk allowed vlan 10,11,20,21<br />
SW1(config-if)#switchport trunk native vlan 999<br />
<br />
SW1(config-if)#int f0/3<br />
SW1(config-if)#switchport trunk allowed vlan 10,11,20,21<br />
SW1(config-if)#switchport trunk native vlan 999<br />
<br />
SW1(config)#int f0/4<br />
SW1(config-if)#switchport access vlan 10<br />
SW1(config-if)#switchport voice vlan 11<br />
<br />
SW1(config-if)#int f0/5<br />
SW1(config-if)#switchport access vlan 20<br />
SW1(config-if)#switchport voice vlan 21<br />
<br />
SW1(config)#int range f0/6-24, g0/1-2
SW1(config-if-range)#switchport access vlan 100
<br />
<img src="https://i.imgur.com/s4hRNOT.png" height="80%" width="80%" />
DHCP
NTP
Syslog
<h3> 2. Distribution Layer</h3>
<h4> A. Distribution Switches</h4>
Hostname and password
Interfaces, Vlans, vlan interfaces, descriptions, Ip addresses, trunk ports
OSPF
VRRP
NTP
DHCP relay
DNS
RADIUS
Syslog
<h3>3. Core Layer</h3>
<h4> A. Core Switches</h4>
See configuration file for process
<h3>4. Cisco ASA</h3>
Hostname and password
Interfaces, description, nameif, security level, ip address
Syslog
Default and static routes
Objects and object groups
ICMMp ECHO permit inside | across networks
SSH
OSPF
Authentication
Security zones
ACLs out-to-in and in-to-out
NTP
RADIUS
<h3>5. Data Center</h3>
<h4> A. Switch</h4>
Hostname and password
point-to-point layer3 links
OSPF
access ports in VLAN50
Etherchannel
NTP
Syslog trap sending
RADIUS authentication
<h4> B. Server</h4>
SSH
Services: DNS, NTP, DHCP, RADIUS, and Syslog
<h3>6. Edge Router and ISPs</h3>
<h4> A. Edge router</h4>
Hostname and password
Username and password privileged exec mode
Interfaces, ip addresses, descriptions
NAT / PAT, ACLs
Static routes
BGP
NTP
Syslog
DNS
SSH, VTY access list
<h4> B. ISP router</h4>
Hostname and password
interfaces, ip addresses, descriptions
BGP
NAT
DNS
<h3>7. DMZ</h3>
<h4> A. ASA </h4>
Hostname and password
Interfaces, description, nameif, security level, ip address
AAA
Default and static routes
Objects and object groups
SSH
ACLs out-to-in and in-to-out
NTP
Syslog
Traffic inspection
Security zones
<h4> B. Switch</h4>
Hostname and password
Username and password privilege exec mode and SSH, line console
interfaces , descriptions, ip addresses
Vlan interface, vlan name, VTP, and SVI port
Static default route
NTP
DNS
Syslog
<h4>C. Server </h4>
NTP
DNS
Web
Syslog
