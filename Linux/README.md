## Important commands 
cat /etc/os-release   ------- To know OS info & release       
cloud_user@joshuamothkur1c:~$ sudo df -h /var/lib/docker/overlay2        
Filesystem      Size  Used Avail Use% Mounted on
/dev/root        20G  4.8G   15G  25% /
cloud_user@joshuamothkur1c:~$ sudo du -sch /var/lib/docker/overlay2
1.7G    /var/lib/docker/overlay2
1.7G    total
Adding a user under sudoer list:     
[root@usplrs00236 eyarred]# echo "eyarred ALL=(root) NOPASSWD:ALL" >> /etc/sudoers.d/    
eyarred    
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
[eyarred@devops3 ~]$ curl https://icanhazip.com    
198.24.6.148



