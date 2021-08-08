# EH-Assignment
Scripts for NP CSF Ethical Hacking Module Assignment

## Requirements

1. Hardware
* minimally 8GB RAM (recommended 12GB and above)

2. VMs
* VMware Workstation Pro 15/16
* [Ubuntu *Server* 14.04.5 iso](https://old-releases.ubuntu.com/releases/14.04.5/)
* Windows 10 2019 iso
* [Kali Linux 2021.1 or newer iso](https://cdimage.kali.org/)

*iso images should be `amd64` to allow for virtualization on Windows

3. Software
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
