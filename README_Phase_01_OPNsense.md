# Phase 01 – Initial Setup of OPNsense Firewall

## Scenario: Small Business Network Initialization

You’ve been hired to set up the network security for a small printing business. The first task is to install the OPNsense firewall and prepare it for future configurations.

---

## Objective
- Install OPNsense on a virtual machine
- Set up WAN and LAN interfaces
- Access the web GUI
- Complete the setup wizard
- Change default root password
- Export and back up the configuration

---

## Why This Phase Matters
This is the foundation of your network. Before you can secure users, set up rules, or control traffic, you must get the firewall installed and accessible.

---

## Tools Used
- VirtualBox
- OPNsense ISO
- Windows 10 VM (for accessing GUI)
- Network: Internal Adapter `LANswitch`, NAT for WAN

---

## Configuration Steps

### 1. Install OPNsense on VirtualBox
- Booted into OPNsense ISO
- Chose guided install (UFS)
- Set root password
- Rebooted and removed ISO

### 2. Assign Network Interfaces
- WAN  `em0` (NAT)
- LAN  `em1` (Internal: LANswitch)
- LAN IP set to `192.168.10.1/24`

### 3. Access Web GUI
- From Windows 10 VM connected to `LANswitch`
- Browsed to `https://192.168.10.1`
- Logged in as `root`

### 4. Setup Wizard
- Hostname: `opnsense-fw`
- DNS: `1.1.1.1`, `8.8.8.8`
- Changed root password
- Confirmed connectivity

### 5. Backup Config
- Downloaded OPNsense config as `phase01-config.xml`

---

## Testing Done
- Windows 10 received IP via DHCP (if enabled in firewall)
- Could ping and browse to the firewall GUI

---

## Included Files
- `phase01-config.xml` - backup of the firewall config


---

## Reflection
This phase set the foundation of your firewall-based network. The IP address scheme and interface layout are essential before proceeding to firewall rules, VLANs, and VPNs.

---

