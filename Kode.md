# intervlan
## S1
en 
conf t
int p 1
sw m t
sw t a v 1,10,20,30,40
int p 3
sw m t
sw t a v 1,10,20,30,40

int g0/1
sw m t
sw t a v 1,10,20,30,40


## S2
en 
conf t
int p 1
sw m t
sw t a v 1,10,20,30,40
int p 2
sw m t
sw t a v 1,10,20,30,40


## S3
en 
conf t
int p 2
sw m t
sw t a v 1,10,20,30,40
int p 3
sw m t
sw t a v 1,10,20,30,40


# VLAN Server-Client
## S1
en 
conf t
vtp mode server
vtp domain JK17
vlan 10
name Engineer
vlan 20
name Finance
vlan 30
name Telco
vlan 40
name R&D


## S2 & S3
en
conf t
vtp mode client
vtp domain JK17

# Access
int f0/_angka_
sw m a
sw a v _vlan_

# DHCP
## RJ
en
conf t
ip dhcp pool VLAN10
 network 192.168.10.0 255.255.254.0
 default-router 192.168.10.1
 dns-server 192.168.14.62
 domain-name jakarta17.com

ip dhcp pool VLAN20
 network 192.168.12.0 255.255.255.0
 default-router 192.168.12.1
 dns-server 192.168.14.62
 domain-name jakarta17.com

ip dhcp pool VLAN30
 network 192.168.13.0 255.255.255.128
 default-router 192.168.13.1
 dns-server 192.168.14.62
 domain-name jakarta17.com

ip dhcp pool VLAN40
 network 192.168.13.128 255.255.255.192
 default-router 192.168.13.129
 dns-server 192.168.14.62
 domain-name jakarta17.com

 
## RS
en
conf t
ip dhcp excluded-address 192.168.14.62

ip dhcp pool VLAN10
 network 192.168.13.192 255.255.255.128
 default-router 192.168.13.193
 dns-server 192.168.14.62
 domain-name singapore17.com

ip dhcp pool VLAN20
 network 192.168.14.64 255.255.255.192
 default-router 192.168.14.65
 dns-server 192.168.14.62
 domain-name singapore17.com

ip dhcp pool VLAN30
 network 192.168.14.128 255.255.255.192
 default-router 192.168.14.129
 dns-server 192.168.14.62
 domain-name singapore17.com

ip dhcp pool VLAN40
 network 192.168.14.192 255.255.255.192
 default-router 192.168.14.193
 dns-server 192.168.14.62
 domain-name singapore17.com

## RN
en
conf t
ip dhcp pool VLAN10
 network 192.168.15.0 255.255.255.192
 default-router 192.168.15.1
 dns-server 192.168.14.62
 domain-name nusantara17.com

ip dhcp pool VLAN20
 network 192.168.15.64 255.255.255.192
 default-router 192.168.15.65
 dns-server 192.168.14.62
 domain-name nusantara17.com

ip dhcp pool VLAN30
 network 192.168.15.128 255.255.255.192
 default-router 192.168.15.129
 dns-server 192.168.14.62
 domain-name nusantara17.com

ip dhcp pool VLAN40
 network 192.168.15.192 255.255.255.224
 default-router 192.168.15.193
 dns-server 192.168.14.62
 domain-name nusantara17.com

# Routeing RIP
## RJ
en
conf t
router rip
 version 2
 no auto-summary
 network 192.168.10.0
 network 192.168.12.0
 network 192.168.13.0
 network 192.168.13.128
 network 192.168.15.224
 network 192.168.15.232
exit

## RS
en
conf t
router rip
 version 2
 no auto-summary
 network 192.168.13.192
 network 192.168.14.64
 network 192.168.14.128
 network 192.168.14.192
 network 192.168.15.232
 network 192.168.15.228 
exit

## RN
en
conf t
router rip
 version 2
 no auto-summary
 network 192.168.15.0
 network 192.168.15.64
 network 192.168.15.128
 network 192.168.15.192
 network 192.168.15.224
 network 192.168.15.228
exit
