# Switch Configuration and Explanation
## Device Details
- Device: Cisco Catalyst 2960 Switch
- Role: LAN Access Switch
- IP Address: 192.168.10.2
- Provides connectivity for PCs, Printer, and Access Point

## Switch Configuration

Click **Switch → Command Prompt**

### 1. Enter Configuration Mode
```bash
enable
configure terminal

### 2. Set Hostname
```bash
hostname SW1
```
### 3. Set Console Password
```bash
line console 0
password cisco
login
exit
```
### 4. Encrypt password
```bash
service password-encryption
```

### 5. Configure Management IP
```bash
interface vlan 1
ip address 192.168.10.2 255.255.255.0
no shutdown
exit
ip default-gateway 192.168.10.1
```

### 6. Disable Unused Ports
```bash
interface range fa0/8-24
shutdown
exit
```

### 7. Save Configuration
```bash
end
copy running-config startup-config
```

### 8. Verify Interfaces
```bash
show ip interface brief
```

### Understanding the above commands
<h3 align="center">Switch CLI Configuration(Security + Management)</h3>

<p align="center">
<img src="../screenshots/switch-interface1.png" alt="Switch CLI Config" width="600">
</p>

<h3 align="center">Switch Save & Verification</h3>

<p align="center">
<img src="../screenshots/switch-interface2.png" alt="Switch Save and Verify" width="600">
</p>

