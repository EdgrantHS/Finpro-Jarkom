# RJ
en
conf t
ip dhcp pool VLAN10
network 192.168.10.0 255.255.254.0
default-router 192.168.10.1

ip dhcp pool VLAN20
network 192.168.12.0 255.255.255.0
default-router 192.168.12.1

ip dhcp pool VLAN30
network 192.168.13.0 255.255.255.128
default-router 192.168.13.1

ip dhcp pool VLAN40
network 192.168.13.128 255.255.255.192
default-router 192.168.13.129

# RS
en
conf t
ip dhcp pool VLAN10
network 192.168.13.192 255.255.255.128
default-router 192.168.13.193

ip dhcp pool VLAN20
network 192.168.14.64 255.255.255.192
default-router 192.168.14.65

ip dhcp pool VLAN30
network 192.168.14.128 255.255.255.192
default-router 192.168.14.129

ip dhcp pool VLAN40
network 192.168.14.192 255.255.255.192
default-router 192.168.14.193

# RN
en
conf t
ip dhcp pool VLAN10
network 192.168.15.0 255.255.255.192
default-router 192.168.15.1

ip dhcp pool VLAN20
network 192.168.15.64 255.255.255.192
default-router 192.168.15.65

ip dhcp pool VLAN30
network 192.168.15.128 255.255.255.192
default-router 192.168.15.129

ip dhcp pool VLAN40
network 192.168.15.192 255.255.255.224
default-router 192.168.15.193

