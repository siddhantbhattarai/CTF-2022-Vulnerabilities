# Vulnerable Ubuntu Server for CTF Practice

Welcome to the **Vulnerable Ubuntu Server CTF Practice Lab**! This project is designed to help students and cybersecurity enthusiasts practice exploiting real-world vulnerabilities in a controlled environment. Below is a complete guide for setting up, running, and using this CTF server.

---

## **Table of Contents**
1. [Overview](#overview)
2. [Pre-requisites](#pre-requisites)
3. [Installation](#installation)
4. [Starting the Server](#starting-the-server)
5. [CTF Challenges](#ctf-challenges)
6. [Tools and Resources](#tools-and-resources)
7. [Security Warnings](#security-warnings)
8. [Contributing](#contributing)

---

## **Overview**
This CTF lab includes simulations of **99 popular CVEs from 2022** using Docker containers. Each container represents a specific vulnerability and runs on unique ports to avoid conflicts.

This lab is structured to:
- Provide hands-on exploitation challenges.
- Teach vulnerability types like **Injection**, **Memory Management Errors**, **Broken Access Control**, **Cryptographic Failures**, and more.

---

## **Pre-requisites**
- Ubuntu Server (20.04 or later recommended)
- Docker and Docker Compose installed
- Basic familiarity with Linux commands and networking

To install Docker and Docker Compose:
```bash
sudo apt update
sudo apt install docker.io docker-compose -y
```

---

## **Installation**

1. Clone this repository:
   ```bash
   git clone https://github.com/your-repo/vulnerable-ctf-server.git
   cd vulnerable-ctf-server
   ```
2. Copy the provided Docker Compose files (`docker-compose.yml` and `docker-compose-additional.yml`) to your project folder.

---

## **Starting the Server**
1. Make the startup script executable:
   ```bash
   chmod +x start_vulnerable_services.sh
   ```
2. Start all services:
   ```bash
   ./start_vulnerable_services.sh
   ```

To confirm services are running:
```bash
docker ps
```
You should see all containers listed and running.

---

## **CTF Challenges**

Each challenge corresponds to a specific CVE and is configured to simulate real-world vulnerabilities. The challenges are divided into two sets:

1. **Primary Set** (Ports: 8080, 443, 80, etc.)
2. **Additional Set** (Ports: 7070, 10001, 8585, etc.)

Detailed documentation for each challenge is available:
- **Primary Challenges:** Refer to `ctf_challenge_documentation.md`
- **Additional Challenges:** Refer to `remaining_ctf_challenges.md`

Each document includes:
- CVE details
- Hints for exploitation
- Suggested tools
- Exploitation steps
- Expected outcome (to confirm success)

---

## **Tools and Resources**

Here are some recommended tools for practicing the CTF challenges:
- **Metasploit Framework:** `https://www.metasploit.com/`
- **Burp Suite:** `https://portswigger.net/burp`
- **Nmap:** `https://nmap.org/`
- **Wireshark:** `https://www.wireshark.org/`
- **GDB Debugger:** `https://sourceware.org/gdb/`

Useful Exploit Sources:
- `https://github.com/offensive-security/exploitdb`
- `https://github.com/swisskyrepo/PayloadsAllTheThings`

---

## **Security Warnings**
- **Isolate the Lab:** This lab is intentionally vulnerable and should never be exposed to the internet.
- **Disable unnecessary network interfaces** to avoid accidental exposure.
- **Use VM snapshots or backups** in case of errors or irreversible changes.

---

## **Contributing**
Contributions are welcome! To suggest improvements:
1. Fork the repository.
2. Create a feature branch.
3. Submit a pull request with a description of your changes.

---

Enjoy your CTF practice and improve your cybersecurity skills!
