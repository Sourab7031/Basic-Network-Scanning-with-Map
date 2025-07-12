# Basic-Network-Scanning-with-Nmap

## Overview
This repository contains the results and documentation of a network scanning exercise conducted using `nmap` on a Kali Linux VirtualBox VM. The scan targets a local network (e.g., `192.168.56.0/24`) to identify open ports and services, which can be used for security assessment or penetration testing tasks like SQL Injection on DVWA.

## Date of Scan
- **Date**: 2025-07-12
- **Time**: 15:06 IST

## Scan Details
- **Tool**: Nmap 7.94
- **Target**: 192.168.56.0/24 (VirtualBox NAT network)
- **Scan Type**: Stealth SYN Scan (`-sS`) with Timing Template 4 (`-T4`)
- **Output File**: `nmap-scan-result.text`

## Scan Results
The scan identified the following hosts and services:
- **192.168.56.101**:
  - Port 80/tcp: `open` (HTTP - likely Apache for DVWA)
  - Port 3306/tcp: `open` (MySQL - likely MariaDB for DVWA)
  - Port 443/tcp: `closed` (HTTPS)
- **192.168.56.1**:
  - Port 22/tcp: `open` (SSH - likely gateway or host machine)
- Total Hosts: 2 out of 256 scanned.

See `nmap-scan-result.text` for the full output.

## Usage
1. Clone this repository: `git clone <repository-url>`
2. Review the `nmap-scan-result.text` file for scan details.
3. Use the results for security testing (e.g., targeting port 80 for DVWA SQL Injection).

## Prerequisites
- Kali Linux VM with `nmap` installed: `sudo apt install nmap -y`
- VirtualBox network configured (NAT or Bridged)

## Installation
1. Ensure `nmap` is installed.
2. Run a scan: `sudo nmap -sS -T4 192.168.56.0/24 -oN nmap-scan-result.text`
3. Update the `README.md` and `nmap-scan-result.text` with your results.

## Contributing
Feel free to fork this repository, add your own scans, or improve the documentation. Submit pull requests with your changes.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- Nmap (https://nmap.org)
- DVWA Project (https://github.com/digininja/DVWA)
