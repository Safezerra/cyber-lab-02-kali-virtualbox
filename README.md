# cyber-lab-02-kali-virtualbox
Beginner cybersecurity lab using Kali Linux and VirtualBox, with setup notes and network verification.

# Cyber Lab #01: Kali Linux on VirtualBox

My first cybersecurity lab project: setting up Kali Linux as a virtual machine on a Windows host using Oracle VirtualBox.

## 🎯 Objective

Build a basic, controlled environment for learning Linux, networking, ethical hacking fundamentals, and authorized cybersecurity testing.

## 🧰 Tools Used

- Windows host machine
- Oracle VirtualBox
- Official Kali Linux pre-built VirtualBox image
- 7-Zip for extracting the downloaded archive

## 🏗️ Lab Architecture

```text
Windows Host
    |
    v
VirtualBox
    |
    v
Kali Linux VM
    |
    v
Network Adapter 1: NAT
```

## ⚙️ Virtual Machine Configuration

Example configuration:

- **RAM:** 4 GB (4096 MB), if the host has enough available memory
- **Processors:** 2
- **Network Adapter 1:** NAT

Resource allocation depends on the host computer. Leave enough CPU and RAM for Windows to run comfortably.

## 🚀 Setup Workflow

1. Download VirtualBox from the official Oracle website.
2. Download the official Kali Linux pre-built VirtualBox image.
3. Install 7-Zip if needed and extract the downloaded `.7z` archive.
4. Add the existing Kali VM to VirtualBox using the appropriate Open/Add option.
5. Configure RAM, processors, and NAT networking.
6. Start Kali Linux.
7. Inspect network interfaces and routes.
8. Update system packages.
9. Create a clean VirtualBox snapshot.

## 🔎 Network Verification Commands

### 1. Inspect Network Interfaces and IP Addresses

```bash
ip addr
```

Shows network interfaces and their IP addresses.

### 2. Inspect the Routing Table

```bash
ip route
```

Shows routing information, including the default route when one is configured.

### 3. Test Basic Connectivity

```bash
ping -c 4 google.com
```

Sends four ping requests to test connectivity. Results depend on network access, DNS resolution, and whether the destination responds to ping.

## 🔄 System Updates

### Update Package Information

```bash
sudo apt update
```

Refreshes information about available packages and updates.

### Install Available Upgrades

```bash
sudo apt full-upgrade -y
```

Installs available upgrades and automatically confirms package prompts. Review package changes and ensure the VM has sufficient free disk space before upgrading.

## 📸 VirtualBox Snapshot

**Snapshot name:** `Clean Kali Setup`

**Purpose:** Preserve a known-good starting state before performing future experiments.

A snapshot can help restore the VM to its saved state after configuration changes or experiments. It is not a replacement for a separate backup.

## 🧠 What I Learned

- A virtual machine runs inside a host computer.
- A pre-built Kali VM can be added without creating a new VM from an ISO.
- RAM and CPU allocation affect both the guest VM and host system.
- NAT is useful for basic outbound internet access.
- Network interfaces and routes can be inspected from the Linux terminal.
- Ping can be used for basic connectivity testing.
- Snapshots help restore a VM to a saved state.

## 🔜 Next Project: Cyber Lab #02

**VirtualBox Networking for Cybersecurity Labs**

Topics to explore:

- NAT
- Bridged Adapter
- Host-only Adapter
- Internal Network
- Host-to-VM communication
- VM-to-VM communication
- Isolated cybersecurity lab design

  Safety and Ethical Practice

This project is for educational purposes and authorized cybersecurity practice.

Only test systems, applications, and networks that you own or have explicit permission to test.

🎥 Project Video

 How to Set Up Your Kali Linux Cybersecurity Lab on VirtualBox

YouTube: [Watch the full tutorial]
  https://youtu.be/FI0RuxmrAYw?si=DjlOBbROr0k7m563




Pehle lab. Phir tools. Phir attacks.
