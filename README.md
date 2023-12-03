<h1>Network Home Lab 2</h1>

<h2>Overall Description</h2>
Simulate enterprise network in Cisco Packet Tracer with various devices such as PCs, switches, routers, firewalls, and servers. Configuration of a three-tier network model, comprising access, distribution, and core layers; as well as a data center and DMZ. 
<br />
<br />
1. Access layer will provide end-users with network access. Key configurations for the access layer include switches with VLANs, IP addresses and trunk ports, SVIs, NTP and syslog configurations, static routes, and passwords. PC configurations involve static IP addresses and default gateways. 
<br />
<br />
2. Distribution layer will provide aggregation of routing and VLANs to facilitate efficient network performance. Key configurations for distribution layer switches include VLANs, IP addresses, trunk ports, SVIs, OSPF, VRRP, NTP, DHCP relay, DNS, RADIUS, and Syslog. 
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
Drag and frop devices as seen in the diagram. Connect devices with appropriate cabling. Run command 'show cdp neighbors' to label interfaces. Label devices with hostnames: <br/>
<img src="https://i.imgur.com/6raWWEw.png" height="80%" width="80%" />
