## Day 1
### Topic: Network Devices
I started with the fundamentals. I learned what a computer network is, the various types of nodes, and how they interact with each other.
I now have a solid understanding of routers, switches, clients, servers, firewalls, and Ethernet.

## Day 2
### Topc: Types of Cabling as defined by Ethernet Standards
Today I learned the basics of Ethernet networking, including data units (bits and bytes), network speeds, IEEE 802.3 standards, UTP cabling, RJ-45 connectors, straight-through cables, Ethernet pinouts, Auto MDI-X, full-duplex communication, and the fundamentals of fiber-optic networking and SFP transceivers. This forms the foundation for my Network Engineering journey.

## Day 3
### Topic: How TCP/IP Actually Works
Today, I dove into how the TCP/IP Protocol Suite actually works to make communication over the internet possible. I focused on understanding the underlying standards, the 5-layer model, and how data changes as it moves through the network.
##### KEY TAKEAWAYS:
Network Standards: Learned that network products rely on vendor-neutral protocols standardized by bodies like the IEEE (handling Ethernet/Wi-Fi) and the IETF via RFCs (like RFC 791).
**The 5-Layer Model**: Broke down the responsibilities of each layer, mapping out how data moves from application processes down to physical hardware transmission:

**Application & Transport**: Managing data creation and end-to-end communication using port numbers (TCP/UDP).

**Internet & Local-Network**: Handling routing across networks using IP and MAC addresses.

**Physical**: Translating everything into raw bits over electrical or optical signals.

**Data Encapsulation**: Tracked how data is wrapped and renamed at each stage of the encapsulation/decapsulation process. I mapped out how data transforms from Segments/Datagrams (Layer 4) into Packets (Layer 3), and finally into Frames (Layer 2)

## Day 4
### Topic: Cisco IOS CLI Basics

​To access the cli( Command line interface) it requires a rollover cable, terminal emulator, or Packet Tracer for simulation.

​**Navigation Modes:**

​Router> (User EXEC) 

​Router# (Privileged EXEC) 

​Router(config)# (Global Configuration)

**​Device Files & Security**

​Files: running-config (active in RAM) and startup-config (saved in NVRAM).

**​Security Commands**

​service password-encryption : Encrypts plain-text passwords.

​enable secret <pass> : Highly secure, recommended method to lock privileged mode.

## Day 5
### Topic: Ethernet LAN Switching

A Local Area Network (LAN) is a network contained within a relatively small geographical area. At the Data Link Layer, data is encapsulated into an Ethernet frame consisting of a header, payload, and trailer.

**Ethernet Frame**
The ethernet header comprises of: 

1. Preamble: Its size is 7 Bytes (56 bits). Some of its characteristics are alternating 1s and 0s and allowng receiving devices to synchronize their receiver clocks.
   
2. SFD: The SFD (Start Frame Delimiter) has a length of 1 byte (8 bits), uses the bit pattern 10101011, and marks the end of the preamble and the beginning of the rest of the frame.
   
3. Destination and Source: The Destination and Source indicate the devices sending and receiving the frame. A MAC (Media Address Control) is a 6 byte (48 bits) address of a physical address.
   
4. Type: The Type or Length is a 2 byte (16 bit) field. If its value is less than or equal to 1500, it is the length of the encapsulated packet, and if it is greater than or equal to 1536, it is the type of the packet.

The ethernet trailer comprises of

1. FCS: The FCS (Frame Check Sequence) in the Ethernet Trailer is 4 bytes (32 bits) and detects corrupted data by running a 'CRC' algorithm over the received data, where CRC stands for Cyclic Redundancy Check.

**Media Accesss Control**

A MAC (Media Access Control) address is a 6-byte (48-bit) physical address assigned to a network interface when it is manufactured.
Some common terms used in MAC are:

-BIA(Burned-In Address): MAC addresses are globally unique hardware addresses assigned to the device.

-OUI(Organizationally Unique Identifier): The initial vendor-specific portion of the MAC address that identifies the manufacturer.

-Known Unicast: If the destination MAC is in the switch's MAC address table, the frame is forwarded directly out of the specific port.

-Unknown Unicast: If the destination MAC is not found in the table, the frame is flooded out of all ports except the incoming port.

-Aging Timer: Dynamic entries in the MAC address table are automatically removed after 5 minutes of inactivity.

**Network Protocols**

ARP (Address Resolution Protocol) is used to discover a layer 2 address (MAC address) of a known layer 3 address (IP address). It consists of two messages, which are the ARP Request and the ARP Reply. A broadcast ARP request uses ffff.ffff.ffff to send out messages to get MAC addresses.Additionally, GNS3 runs actually CISCO IOS.

Ping is a network utility that is used to test reachability, and it measures round-trip time. It uses two messages: the ICMP Echo Request and the ICMP Echo Reply, where ICMP stands for Internet Control Message Protocol.

Finally, for the tables, the MAC-address table contains the VLAN, Mac address, type, and port, while the ARP-table contains the Internet address, physical address, and type.
