# pfsense_log_parser


Before installation, you must configure **pfSense** to send filter logs (firewall logs) to the machine where you will run the Python script.

In the pfSense web interface, go to:
Status → System Logs → Settings

At the bottom, locate **Remote log servers** and enter the IP address of the machine running the script, along with port **514**.

Under **Remote Syslog Contents**, check:
Firewall Events
Save the changes.

Now, on your configured machine, run the Python script. You should start receiving and processing pfSense firewall logs.


<img width="521" height="796" alt="Image" src="https://github.com/user-attachments/assets/fe4cb953-4d7a-41f1-81d4-008f26387ddd" />



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
git clone https://github.com/oyelaa99/log_parser_code.git
cd log_parser_code
chmod +x firewall_log_parser.py
