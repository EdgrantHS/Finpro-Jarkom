# SJ1
en
conf t 
int r F0/1-2 
channel-group 1 mode active 

int r F0/5-6 
channel-group 3 mode active

# SJ2
en
conf t 
int r F0/1-2 
channel-group 1 mode active

int r F0/3-4 
channel-group 2 mode active 

# SJ3
en
conf t 
int r F0/3-4 
channel-group 2 mode active

int r F0/5-6 
channel-group 3 mode active 
