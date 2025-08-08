# pfsense_log_parser


# pfSense Firewall Log  - Minimal JSON Format

A Python script to decode **pfSense firewall syslog messages** received via UDP port 514.  
Outputs a **minimal JSON** containing:

- `timestamp`
- `src_ip`
- `dst_ip`
- `src_port`
- `dst_port`
- `protocol`
- `action`
- `direction`

---

## Features

- Parses raw **pfSense filterlog** syslog entries.
- Extracts only **key network details**.
- Supports both live syslog listening and test mode.
- Works with **IPv4** and **IPv6** addresses.
- Lightweight and no external dependencies beyond Python's standard library.

---

## Requirements

- Python **3.7+**
- A pfSense firewall sending syslogs to this machine on UDP port **514**.

---

## Installation

```bash
git clone https://github.com/oyelaa99/pfsense_log_parser_code.git
cd pfsense-firewall-decoder
chmod +x pfsense_log_parser_code.py
