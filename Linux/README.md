## Important commands
   cat /etc/os-release
   uname -a    
   hostname -i    
   hostname  

   df -h /var/lib/docker/overlay2            
   du -sch /var/lib/docker/overlay2

   echo "eyarred ALL=(root) NOPASSWD:ALL" >> /etc/sudoers.d/       

   netstat -lntp      
   passwd yreddy1    
   ifconfig ens192        
   curl https://icanhazip.com   

   echo command usage:    
   $ echo "[group1]" > myhosts    
   $ echo "host01 ansible_ssh_user=ubuntu" >> myhosts    
   $ ls    
     myhosts    
   $ cat myhosts    
    [group1]    
    host01 ansible_ssh_user=ubuntu    

  To remove specific entry from known_hosts
  ssh-keygen -R 192.168.19.1 -f /home/mahesh/.ssh/known_hosts    
  OR    
  ssh-keygen -R [192.168.19.1]:2024 -f /home/mahesh/.ssh/known_hosts    
