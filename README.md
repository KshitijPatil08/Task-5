# Task-5
Capture and Analyze Network Traffic Using Wireshark

##  Objective
To perform a live network capture using Wireshark and identify different types of network traffic and protocols.

##  Tools Used
- Wireshark (on Kali Linux/Windows)
- Internet browser and ping commands to generate traffic

##  Procedure

1. Installed Wireshark on my system.
2. Started a packet capture on the active network interface.
3. Browsed a few websites and ran a `ping` command to create traffic.
4. Captured network activity for about 1 minute.
5. Applied protocol filters like `http`, `dns`, `icmp`, and `tcp` to inspect traffic types.
6. Identified multiple protocols used in everyday communication.
7. Exported the capture as a `.pcap` file and analyzed the packet data.

---

##  Protocols Identified

### 1. **DNS (Domain Name System)**
- Translates domain names (like `google.com`) into IP addresses.
- Seen during website browsing.
- Protocol: UDP port 53

### 2. **ICMP (Internet Control Message Protocol)**
- Used in ping operations to test connectivity.
- Echo requests and echo replies were captured.
- Protocol: ICMP type 8 (request), type 0 (reply)

### 3. **HTTP (HyperText Transfer Protocol)**
- Used to access websites.
- HTTP GET and response packets captured.
- Protocol: TCP port 80

### 4. **TCP (Transmission Control Protocol)**
- Underlying transport for HTTP and other protocols.
- Three-way handshake observed: SYN → SYN-ACK → ACK
- Seen in reliable data transfers.

---

##  Findings & Analysis

- DNS requests showed hostname resolutions.
- ICMP packets proved connectivity with external servers.
- HTTP packets revealed unencrypted web requests and headers.
- TCP sessions followed expected SYN/ACK/FIN sequences.
- Some `Info` packets showed retransmissions, likely due to small packet loss.

---

##  Deliverables

- `capture.pcap`: Packet capture file with the filtered and raw traffic.
- `screenshots/`: Images showing packet filtering and analysis.
- `README.md`: This report file.

---

##  Key Concepts Learned

- How to use Wireshark to capture live traffic.
- How to filter and inspect protocol-level packet data.
- Understanding of how different layers of the network stack interact.
