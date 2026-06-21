# Network Topology
![SOHO Network Topology](topology.png)

*In this project the network follows a star topology, where all the other devices are connected to a central switch making it easier to manage, troubleshoot and expand. Devices connected to switch are end devices like PC, Printer and Access Point.* 

- Access Points are generally used for wireless connections for devices such as laptops and tablet although in this lab we've used laptop as the wireless device connected via signal to the AP. 
- The printer is shared across the network and hence provided static IP and configurations.
- Router acts like the default gateway and provides DHCP services to all the end devices or say client devices. 
- The ISP cloud is connected to the router to represent internet connectivity.

#### Device Count and Connections
- 1 × ISP Cloud (Cloud-PT)
- 1 × Cisco 1941 Router
- 1 × Cisco 2960 Switch
- 1 × Access Point-PT-AC
- 5 × Wired PCs
- 3 × Wireless Laptops
- 1 × Network Printer

#### Connections
- Cloud-PT (Eth6) → Router (GigabitEthernet0/0)
- Router (GigabitEthernet0/1) → Switch (FastEthernet0/7)
- Switch (FastEthernet0/1–FastEthernet0/5) → PCs (PC0–PC4)
- Switch (FastEthernet0/6) → Printer
- Switch → Access Point-PT-AC
- Access Point-PT-AC → Laptop0, Laptop1, and Laptop2 (wireless)
