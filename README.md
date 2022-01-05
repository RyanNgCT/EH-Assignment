# EH-Assignment
Scripts for NP CSF Ethical Hacking Module Assignment.

Assignment demonstrates SambaCry (CVE-2017-7494) and ZeroLogon (CVE-2020-1472). Designed to replicate an enterprise pentest/attack scenario.

 The **Simulated** Attack includes the following components
- Scanning and Enumeration
- Exploitation
- Pivoting
- Post-Exploitation Activities

> **Disclaimer:** The author is **NOT** responsible to any breach of computer system(s) and/or violation of National or International Computer Security Laws by third parties (you) accessing this material, including but not limited to _Singapore Computer Misuse and Cybersecurity Act Chapter 50A_. By viewing this material, you agree to not use this for malicious intent and for the sole reason of educational purposes only.


## Case Scenario

> Mel is a disgruntled employee of Company13. During COVID-19, the company deployed the Hamachi VPN service to allow employees to work from home, to access the company file shares via the Samba protocol hosted on an Ubuntu File server. 

> Mel decides to use this opportunity to attack the outdated version of Samba and compromise the server using SambaCry. Since the Samba File Server has an interface communicating with Active Directory Domain, Mel can pivot to and exploit the Domain Controller with the Zerologon vulnerability to steal domain credentials and exfiltrate the company’s data.

## Network Diagram
![image](https://user-images.githubusercontent.com/48358569/148192373-c956e21f-d2b9-49fe-aaae-99c3610693ef.png)

## Requirements

#### 1. Hardware
* minimally 8GB RAM (recommended 12GB and above)

#### 2. VMs
* VMware Workstation Pro 15/16
* [Ubuntu *Server* 14.04.5 iso](https://old-releases.ubuntu.com/releases/14.04.5/)
* Windows 10 Server 2019 iso
* [Kali Linux 2021.1 or newer iso](https://cdimage.kali.org/)

_*iso images should be `amd64` to allow for virtualization on Windows_

#### 3. Software
* [Hamachi VPN](https://www.vpn.net/linux) - install on **Kali and Ubuntu** only.
* Kali: Impacket, sshuttle (and dependencies)
* Ubuntu: openssh server, samba (during installation)

a) kali dependencies
```
$ sudo apt update && upgrade -y
$ sudo apt install python3 python3-pip
```

b) Impacket (please refer to [installation guide](https://github.com/SecureAuthCorp/impacket) for newer versions).
```
$ git clone https://github.com/SecureAuthCorp/impacket.git
$ cd impacket
$ python3 -m pip install .
$ sudo pip install virtualenv
$ virtualenv --python=python3 impacket
$ source impacket/bin/activate
$ pip install --upgrade pip
$ pip install .
```
