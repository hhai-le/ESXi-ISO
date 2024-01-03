# Custom VMware ESXi ISO for automated installation

This script help you can custom ESXi ISO:

Clone this repo & upload ESXi ISO which you want to custom:

> git clone https://github.com/hhai-le/ESXi-ISO.git \
> cd ESXi-ISO \
> chmod +x esxi_customks_iso.sh

upload VMware ESXi ISO to this folder.

## example directory

![Alt text](image/image.png)

run script:

```bash
  sudo ./esxi_customks_iso.sh --iso <iso> \
  --ks KS-TEMPLATE.CFG \
  --ip-address <ip of esxi host> \
  --netmask <netmask> \
  --gateway <gateway> \
  --hostname <esxi hostname> \
  --vlan <vlan config for network management if trunking> \
  --dns <nameserver>
```

## example script

```bash
 sudo ./esxi_customks_iso.sh --iso VMware-VMvisor-Installer-7.0U3n-21930508.x86_64.so \
 --ks KS-TEMPLATE.CFG \
 --ip-address 192.168.86.132 \
 --netmask 255.255.255.0 \
 --gateway 192.168.86.1 \
 --hostname esx1-test.j.local \
 --vlan 0 \
 --dns 172.16.11.5
```

