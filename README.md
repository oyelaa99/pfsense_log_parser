# pfsense_log_parser



before the installation you should configure pfsense to send filter log (firewall log ) to the machine where you are going to run the code 
in your pfsense web interface.
go to status/system logs/settings/ at the buttom you will see **Remote log servers** 
put the ip of the machine where your are going to run the script and the port 514  below you'll see **Remote Syslog Contents** 
check **Firewall Events** and save the change now you can go in your machine and run the python code . 
you will see the following information 



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
