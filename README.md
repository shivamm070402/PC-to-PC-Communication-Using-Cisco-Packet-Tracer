# Connect 2 PCs and Test Communication Using Ping (Cisco Packet Tracer)

## 📌 Objective

This lab demonstrates how to:

- Connect two PCs using a Cisco 2960 switch
- Configure static IPv4 addresses
- Verify network connectivity using the `ping` command
- Understand basic Local Area Network (LAN) communication

---

## 📖 Theory

### What is Ping?

`ping` is a network utility used to test connectivity between two devices on an IP network.

It uses the **Internet Control Message Protocol (ICMP)** to send **Echo Request** packets and receive **Echo Reply** packets.

If the destination responds, the devices are communicating successfully.

---

## 🛠️ Requirements

- Cisco Packet Tracer
- 2 PCs
- Cisco 2960 Switch
- Copper Straight-Through Cables

---

## 🌐 Network Topology
<img width="711" height="244" alt="image" src="https://github.com/user-attachments/assets/35bb7133-6741-4db3-8038-9f3f0c02b225" />





---

## 🚀 Step 1: Open Cisco Packet Tracer

Launch Cisco Packet Tracer.

---

## 🖥️ Step 2: Add Devices

### End Devices

- PC0
- PC1

### Switches

- Cisco 2960 Switch

---

## 🔌 Step 3: Connect Devices

Choose:

**Connections (⚡) → Copper Straight-Through Cable**

Connect:

```text
PC0 FastEthernet0  --->  Switch FastEthernet0/1

```
<img width="264" height="162" alt="image" src="https://github.com/user-attachments/assets/1692b82c-ccf2-4043-b3c2-069389028783" />

```text
PC1 FastEthernet0  --->  Switch FastEthernet0/2
```
<img width="269" height="110" alt="image" src="https://github.com/user-attachments/assets/8c35b34d-042e-435d-b901-65fd862672e1" />

Wait until both links turn **green**.

---

## 🌍 Step 4: Configure PC0

Navigate to:

<img width="702" height="298" alt="image" src="https://github.com/user-attachments/assets/b105763f-3d8e-4868-a8f2-8659afe79030" />
**PC0 → Desktop → IP Configuration**

| Field | Value |
|-------|-------|
| IP Address | 192.168.1.10 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | Leave Blank |


---

## 🌍 Step 5: Configure PC1

Navigate to:

**PC1 → Desktop → IP Configuration**

| Field | Value |
|-------|-------|
| IP Address | 192.168.1.20 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | Leave Blank |

---

## 📋 IP Address Table

| Device | IP Address | Subnet Mask |
|---------|------------|-------------|
| PC0 | 192.168.1.10 | 255.255.255.0 |
| PC1 | 192.168.1.20 | 255.255.255.0 |

---

## 🧪 Step 6: Test Connectivity

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

If both commands receive replies, the network is working correctly.

---

## 📡 Packet Flow

```text
PC0
 │
 │ ICMP Echo Request
 ▼
Switch
 │
 ▼
PC1

PC1
 │
 │ ICMP Echo Reply
 ▼
Switch
 │
 ▼
PC0
```

---

## 🔍 Troubleshooting

### Problem: Request Timed Out

Possible causes:

- Incorrect cable type
- Wrong port connections
- Incorrect IP addresses
- Different subnet masks
- Switch ports not yet active

---

### Problem: Destination Host Unreachable

Possible causes:

- Devices are in different networks
- Incorrect IP configuration
- Disabled network interface

---

## 📚 Concepts Learned

- Computer Networks
- Local Area Network (LAN)
- Cisco Packet Tracer
- Static IPv4 Addressing
- Subnet Mask
- ICMP Protocol
- Ping Command
- Basic Network Troubleshooting

---

## 💡 Mini Project

Build the following topology:

```text
          Switch
        /    |    \
     PC0    PC1   PC2
```

Assign the following IP addresses:

| Device | IP Address |
|---------|------------|
| PC0 | 192.168.1.10 |
| PC1 | 192.168.1.20 |
| PC2 | 192.168.1.30 |

Subnet Mask:

```text
255.255.255.0
```

Verify communication by pinging every PC from the others.

---

## 🎯 Learning Outcomes

After completing this lab, you will be able to:

- Build a simple LAN in Cisco Packet Tracer
- Connect devices through a switch
- Configure static IPv4 addresses
- Test connectivity using the `ping` command
- Understand ICMP communication
- Troubleshoot basic network issues

---

## 🛠️ Tools Used

- Cisco Packet Tracer
- Cisco 2960 Switch
- End Devices (PCs)

---

## 📂 Project Structure

```text
Connect-2-PCs-Ping/
│
├── README.md
├── Connect_2_PCs.pkt
└── screenshots/
    ├── topology.png
    ├── ip_configuration.png
    └── ping_success.png
```

---

## 📸 Screenshots

Add screenshots for:

- Network Topology
- IP Configuration
- Successful Ping Output

---

## 📄 License

This project is created for educational and learning purposes.
