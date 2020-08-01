# Important commands 
cat /etc/os-release   ------- To know OS info & release    

__ df -h and du -sch usage: __    
cloud_user@joshuamothkur1c:~$ sudo df -h /var/lib/docker/overlay2    
Filesystem      Size  Used Avail Use% Mounted on
/dev/root        20G  4.8G   15G  25% /
cloud_user@joshuamothkur1c:~$ sudo du -sch /var/lib/docker/overlay2
1.7G    /var/lib/docker/overlay2
1.7G    total

Adding a user under sudoer list:
[root@usplrs00236 eyarred]# echo "eyarred ALL=(root) NOPASSWD:ALL" >> /etc/sudoers.d/eyarred

[eyarred@usplrs00235 ~]$ uname -a
Linux usplrs00235.bete.ericy.com 4.19.6-1.el7.elrepo.x86_64 #1 SMP Sat Dec 1 11:58:18 EST 2018 x86_64 x86_64 x86_64 GNU/Linux

netstat -lntp   ---> To know the ports which mapped
How to change password:
root@dds1 ~ # passwd yreddy1
Changing password for user yreddy1.
New password:
BAD PASSWORD: The password fails the dictionary check - it is based on a dictionary word
Retype new password:
passwd: all authentication tokens updated successfully.

How to check IP:
[eyarred@devops3 ~]$ ifconfig ens192
ens192: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 10.125.210.86  netmask 255.255.255.240  broadcast 10.125.210.95
        inet6 fe80::250:56ff:fe8b:13bb  prefixlen 64  scopeid 0x20<link>
        ether 00:50:56:8b:13:bb  txqueuelen 1000  (Ethernet)
        RX packets 28563023136  bytes 28841744328796 (26.2 TiB)
        RX errors 0  dropped 48044  overruns 0  frame 0
        TX packets 22434996802  bytes 40190448395130 (36.5 TiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

[eyarred@devops3 ~]$ curl https://icanhazip.com
198.24.6.148



