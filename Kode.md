# RJ
en
conf t
hos SS1
no ip domain lookup
ip domain name singapore17.com

service password

banner motd #Unauthorized access prohibited#

line cons 0
exec-timeout 10 0
exit
line vty 0 15
exec-timeout 10 0
exit

do copy run start



# RS
en
conf t
hos RS
no ip domain lookup
ip domain name singapore17.com

# RN
en
conf t
hos RN
no ip domain lookup
ip domain name nusantara17.com