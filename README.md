# Network Traffic Analysis using Wireshark – ICMP, DNS, and TCP Handshake

## Objective
This project analyzes real-time network traffic captured using **Wireshark** to understand how fundamental protocols work during daily networking tasks like browsing or pinging. The protocols analyzed include:

- **ICMP** – Echo Requests/Replies (ping)
- **DNS** – Name resolution for domain lookup
- **TCP** – 3-way handshake and secure connection initiation

---

## Tools & Technologies

| Tool                | Purpose                                   |
|---------------------|-------------------------------------------|
| Wireshark           | Packet sniffing and protocol analysis     |
| Chrome Browser      | Generating DNS and TCP (HTTPS) traffic    |
| Command Prompt (ping)| Generating ICMP echo requests             |
| .pcapng File        | Contains captured network traffic         |

---

## Project Files

| File Name                    | Description                              |
|-----------------------------|------------------------------------------|
| `Wireshark_Traffic.pcapng`  | Raw capture file from Wireshark          |
| `Wireshark_Traffic_Report.pdf` | Detailed protocol analysis report        |
| `Screenshots/`              | Contains protocol-specific screenshots   |

---

## Protocols Analyzed

###  ICMP (Ping)
- Captured echo requests and replies to Google's IP (8.8.8.8)
- Analyzed packet structure: MAC, IP, ICMP headers
- Observed round-trip time (~72ms) and TTL values

###  DNS
- DNS lookups for domains like `www.youtube.com`
- Resolution through A and CNAME records
- Load balancing observed via multiple IP responses

### TCP Handshake
- Captured 3-way TCP handshake (SYN → SYN-ACK → ACK)
- Inspected MSS, SACK, window scaling, sequence numbers
- Observed TLS `Client Hello` immediately after handshake

---

## Skills Demonstrated

- Wireshark Filtering & Packet Inspection
- Protocol-Level Network Troubleshooting
- Understanding TCP/IP Stack and Encapsulation
- Recognizing Modern DNS and TCP Optimization Techniques
- Analyzing Secure TLS Communication after TCP

---

## Screenshots

> Navigate to the `Screenshots/` folder for:
- ICMP request/reply filters
- DNS query & response structure
- TCP handshake flags and headers

---

##  How to View .pcapng File

1. Download and install [Wireshark](https://www.wireshark.org/download.html)
2. Open `Wireshark_Traffic.pcapng`
3. Apply filters:
   - ICMP: `icmp`
   - DNS: `dns`
   - TCP SYN: `tcp.flags.syn == 1 && tcp.flags.ack == 0`
   - Full TCP: `tcp`

---

## Future Enhancements

- Automate packet parsing with **Tshark or Scapy (Python)**
- Extend project to include **ARP**, **HTTPS**, or **HTTP/2**
- Create dashboard for live packet stats using **Grafana**

---

##  Author

**Vedant Tarade**  
_BCA Graduate | Aspiring Network Engineer_  
🔗 [LinkedIn](#) • 🔗 [GitHub](https://github.com/vedant-tarade)

---
