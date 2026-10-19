# CodeAlpha_ProjectName
A basic network sniffer built in Python with Scapy. It captures live
packets, analyzes their structure, and prints useful details.

## Features
- Captures live network traffic
- Shows timestamp, source IP, destination IP, protocol and ports
- Identifies TCP, UDP and ICMP packets
- Displays the first 50 bytes of each payload
- Prints a protocol summary at the end

## Requirements
- Python 3
- Scapy: `pip install scapy`
- Windows: install [Npcap](https://npcap.com) and run as Administrator
- Linux/Mac: run with `sudo`

## How to run
    python sniffer.py

## Sample output
(<img width="865" height="459" alt="snifffff3" src="https://github.com/user-attachments/assets/c81d5a4d-da8e-4035-be91-8cd2839a6ef4" />
)

<img width="923" height="482" alt="snifffff" src="https://github.com/user-attachments/assets/808e95d4-c401-493c-aa31-eaedd89e6f32" />

<img width="903" height="476" alt="snifffff 2" src="https://github.com/user-attachments/assets/df8d5883-4c5e-4365-8aff-3b2b9e7ecfdf" />


## What I learned
- Packets have layers: IP, then TCP/UDP/ICMP, then payload
- HTTPS and QUIC payloads are encrypted, so they look like random bytes
- ICMP (ping) payloads are unencrypted and readable

## Disclaimer
Use this only on networks you own or have permission to monitor.
