
# Connect 2 PCs and Test Communication Using Ping (Cisco Packet Tracer)

A beginner-friendly Cisco Packet Tracer lab demonstrating how to build a simple Local Area Network (LAN), assign static IPv4 addresses, and verify connectivity using the `ping` command.

---

## 📌 Objective

After completing this lab, you will be able to:

- Connect two PCs using a Cisco 2960 switch.
- Configure static IPv4 addresses.
- Test connectivity using the `ping` command.
- Understand basic LAN communication.
- Perform basic network troubleshooting.

---

## 📖 Theory

### What is Ping?

`ping` is a network diagnostic utility used to test connectivity between two devices on an IP network.

It uses the **Internet Control Message Protocol (ICMP)** to send **Echo Request** packets and receive **Echo Reply** packets. If the destination replies, the communication between the devices is successful.

---

## 🛠️ Requirements

- Cisco Packet Tracer
- 2 PCs
- Cisco 2960 Switch
- Copper Straight-Through Cables

---

## 🌐 Network Topology

<img width="711" height="244" alt="Network Topology" src="https://github.com/user-attachments/assets/35bb7133-6741-4db3-8038-9f3f0c02b225" />

---

# 🚀 Practical Steps

## Step 1: Open Cisco Packet Tracer

Launch Cisco Packet Tracer.

---

## Step 2: Add Devices

### End Devices

- PC0
- PC1

### Switches

- Cisco 2960 Switch

---

## Step 3: Connect Devices

Select:

**Connections (⚡) → Copper Straight-Through Cable**

Connect **PC0** to the switch.

```text
PC0 FastEthernet0  --->  Switch FastEthernet0/1
```

<img width="264" height="162" alt="PC0 Connection" src="https://github.com/user-attachments/assets/1692b82c-ccf2-4043-b3c2-069389028783" />

Connect **PC1** to the switch.

```text
PC1 FastEthernet0  --->  Switch FastEthernet0/2
```

<img width="269" height="110" alt="PC1 Connection" src="https://github.com/user-attachments/assets/8c35b34d-042e-435d-b901-65fd862672e1" />

> **Note:** Wait until both switch ports turn **green** before proceeding.

---

## Step 4: Configure PC0

Navigate to:

**PC0 → Desktop → IP Configuration**

| Field | Value |
|-------|-------|
| IP Address | 192.168.1.10 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | Leave Blank |

<img width="702" height="298" alt="PC0 IP Configuration" src="https://github.com/user-attachments/assets/b105763f-3d8e-4868-a8f2-8659afe79030" />

---

## Step 5: Configure PC1

Navigate to:

**PC1 → Desktop → IP Configuration**

| Field | Value |
|-------|-------|
| IP Address | 192.168.1.20 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | Leave Blank |

<img width="676" height="297" alt="PC1 IP Configuration" src="https://github.com/user-attachments/assets/ad094b1b-4755-4b48-9b54-23dd5e4c749c" />

---

## 📋 IP Address Table

| Device | IP Address | Subnet Mask |
|---------|------------|-------------|
| PC0 | 192.168.1.10 | 255.255.255.0 |
| PC1 | 192.168.1.20 | 255.255.255.0 |

---

## Step 6: Test Connectivity

Open:

**PC0 → Desktop → Command Prompt**

Run:

```bash
ping 192.168.1.20
```

Expected Output:

```text
Pinging 192.168.1.20 with 32 bytes of data:

Reply from 192.168.1.20: bytes=32 time<1ms TTL=128
Reply from 192.168.1.20: bytes=32 time<1ms TTL=128
Reply from 192.168.1.20: bytes=32 time<1ms TTL=128
Reply from 192.168.1.20: bytes=32 time<1ms TTL=128

Ping statistics:
    Packets: Sent = 4
              Received = 4
              Lost = 0 (0% loss)
```

Now test from **PC1**:

```bash
ping 192.168.1.10
```

If both devices receive replies, the LAN has been configured successfully.

---

## 📡 Packet Flow

### ICMP Echo Request

<img width="741" height="220" alt="ICMP Echo Request" src="https://github.com/user-attachments/assets/51d51410-684e-4a40-b156-d34c23e91590" />

### ICMP Echo Reply

<img width="724" height="239" alt="ICMP Echo Reply" src="https://github.com/user-attachments/assets/5dfa9668-5dc2-4db9-94f4-94abfc1c7586" />

---

# 🔍 Troubleshooting

## ❌ Problem: Request Timed Out

### Possible Causes

- Incorrect cable type
- Wrong port connections
- Incorrect IP addresses
- Different subnet masks
- Switch ports are still initializing

### Solutions

- Use **Copper Straight-Through** cables.
- Verify all cable connections.
- Ensure both PCs are in the same subnet.
- Verify the subnet mask (`255.255.255.0`).
- Wait until all switch LEDs turn **green**.

---

## ❌ Problem: Destination Host Unreachable

### Possible Causes

- Devices are on different networks.
- Incorrect IP configuration.
- Disabled network interface.

### Solutions

- Ensure both devices belong to the **192.168.1.0/24** network.
- Recheck IP addresses.
- Verify FastEthernet interfaces are enabled.
- Check cable connections.

---

# 📚 Concepts Learned

- Computer Networks
- Local Area Network (LAN)
- Cisco Packet Tracer
- Cisco 2960 Switch
- Static IPv4 Addressing
- IPv4 Subnetting Basics
- ICMP Protocol
- Ping Command
- End-to-End Connectivity Testing
- Basic Network Troubleshooting

---

# 🎯 Learning Outcomes

Upon completing this lab, you can:

- Build a simple LAN in Cisco Packet Tracer.
- Connect hosts using a Layer 2 switch.
- Configure static IPv4 addresses.
- Test connectivity using `ping`.
- Understand ICMP Echo Request and Echo Reply.
- Troubleshoot common LAN connectivity issues.

---

# 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| Cisco Packet Tracer | Network Simulation |
| Cisco 2960 Switch | Layer 2 Switching |
| End Devices (PCs) | Network Hosts |
| Command Prompt | Connectivity Testing |

---

# 📂 Project Structure

```text
Connect-2-PCs-Ping/
│
├── README.md
├── Connect_2_PCs.pkt
└── screenshots/
    ├── topology.png
    ├── cable_connections.png
    ├── ip_configuration_pc0.png
    ├── ip_configuration_pc1.png
    ├── icmp_request.png
    ├── icmp_reply.png
    └── ping_success.png
```

---



