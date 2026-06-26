# PC-to-PC Communication Using Cisco Packet Tracer

## 📌 Project Overview

This project demonstrates how to connect two PCs using a Layer 2 switch in Cisco Packet Tracer, configure IPv4 addresses, and verify network connectivity using the `ping` command. It is a beginner-friendly networking lab that introduces basic LAN communication concepts.

---

## 🎯 Objective

- Connect two PCs through a Cisco 2960 switch.
- Configure IPv4 addresses on both PCs.
- Verify communication using the `ping` command.
- Understand how devices communicate within the same subnet.

---

## 🛠️ Tools Used

- Cisco Packet Tracer
- Windows Command Prompt (inside Packet Tracer)

---

## 📋 Devices Used

| Device | Quantity |
|---------|----------|
| PC | 2 |
| Cisco 2960 Switch | 1 |
| Copper Straight-Through Cable | 2 |

---

## 🌐 Network Topology

```text
                   Ethernet                  Ethernet

+-----------+                         +-------------+                         +-----------+
|    PC0    |-------------------------|   Switch0   |-------------------------|    PC1    |
+-----------+                         +-------------+                         +-----------+

IP Address: 192.168.1.1                                        IP Address: 192.168.1.2
Subnet Mask: 255.255.255.0                                     Subnet Mask: 255.255.255.0
```

---

## 📑 IP Addressing Table

| Device | Interface | IP Address | Subnet Mask |
|---------|-----------|------------|-------------|
| PC0 | FastEthernet0 | 192.168.1.1 | 255.255.255.0 |
| PC1 | FastEthernet0 | 192.168.1.2 | 255.255.255.0 |

---

# Configuration Steps

## Step 1: Create a New Project

- Open Cisco Packet Tracer.
- Create a new workspace.

---

## Step 2: Add Devices

- Add two PCs.
- Add one Cisco 2960 switch.

---

## Step 3: Connect Devices

Use **Copper Straight-Through Cable**.

| From | To |
|------|----|
| PC0 FastEthernet0 | Switch FastEthernet0/1 |
| PC1 FastEthernet0 | Switch FastEthernet0/2 |

Wait until both links become green.

---

## Step 4: Configure PC0

Desktop → IP Configuration

| Setting | Value |
|----------|-------|
| IP Address | 192.168.1.1 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | Leave Blank |

---

## Step 5: Configure PC1

Desktop → IP Configuration

| Setting | Value |
|----------|-------|
| IP Address | 192.168.1.2 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | Leave Blank |

---

## Step 6: Verify IP Configuration

On PC0

```bash
ipconfig
```

Expected

```text
IP Address.......192.168.1.1
Subnet Mask......255.255.255.0
```

On PC1

```bash
ipconfig
```

Expected

```text
IP Address.......192.168.1.2
Subnet Mask......255.255.255.0
```

---

## Step 7: Test Connectivity

From PC0

```bash
ping 192.168.1.2
```

Expected Output

```text
Reply from 192.168.1.2
Reply from 192.168.1.2
Reply from 192.168.1.2
Reply from 192.168.1.2

Packets: Sent = 4, Received = 4, Lost = 0
```

From PC1

```bash
ping 192.168.1.1
```

Expected Output

```text
Reply from 192.168.1.1
```

---

## 🔍 Simulation Mode

Switch to **Simulation Mode** in Cisco Packet Tracer.

Observe the following packet flow:

1. ARP Request
2. ARP Reply
3. ICMP Echo Request
4. ICMP Echo Reply

This confirms successful communication between both PCs.

---

## 📂 Project Structure

```
PC-to-PC-Communication/
│
├── README.md
├── PC_to_PC_Communication.pkt
├── images/
│   ├── topology.png
│   ├── ping_pc0.png
│   ├── ping_pc1.png
│   └── simulation.png
└── architecture.drawio
```

---

## 📸 Screenshots to Include

- Network topology
- IP configuration of PC0
- IP configuration of PC1
- Successful ping from PC0
- Successful ping from PC1
- Simulation mode packet flow

---

## 📚 Networking Concepts Learned

- Local Area Network (LAN)
- IPv4 Addressing
- Subnet Mask
- Layer 2 Switching
- Ethernet Communication
- ARP (Address Resolution Protocol)
- ICMP (Ping)
- End-to-End Connectivity Testing

---

## 🎓 Learning Outcomes

After completing this project, you will be able to:

- Build a simple LAN using Cisco Packet Tracer.
- Connect devices using the correct Ethernet cable.
- Configure IPv4 addressing.
- Verify network configuration using `ipconfig`.
- Test communication using `ping`.
- Analyze ARP and ICMP packets in Simulation Mode.

---

## 🚀 Future Improvements

- Connect four or more PCs.
- Configure VLANs.
- Add a router for inter-network communication.
- Implement DHCP.
- Configure static routing.
- Explore dynamic routing protocols.

---

## 📖 Conclusion

This lab demonstrates the fundamentals of computer networking by connecting two PCs through a Layer 2 switch. Proper IP configuration and successful `ping` responses confirm that devices within the same subnet can communicate without requiring a router. This project builds a strong foundation for more advanced networking and cybersecurity labs.
