```
[root@vdds-cicd ~]# docker run -d --name ansible-container --restart always -it -v /project/manadevops/ansible:/tmp/ansible     maheshreddy7607/docker-ansible:2.9-1-alpine /bin/bash
364c6d3ad6166c31192f8d5cb68a500e87baaac684eb702ba96ff12e1136b74e
[root@vdds-cicd ~]# docker ps
CONTAINER ID        IMAGE                                         COMMAND             CREATED             STATUS              PORTS               NAMES
364c6d3ad616        maheshreddy7607/docker-ansible:2.9-1-alpine   "/bin/bash"         4 seconds ago       Up 3 seconds                            ansible-container
[root@vdds-cicd ~]# docker attach 364
bash-5.0# cd /tmp/ansible/
bash-5.0# pwd
/tmp/ansible
bash-5.0# ls
hosts       sample.yml
bash-5.0# ansible-playbook sample.yml
[WARNING]: No inventory was parsed, only implicit localhost is available

[WARNING]: provided hosts list is empty, only localhost is available. Note that the implicit localhost does not match 'all'


PLAY [This is to make sure connectivity is working] *********************************************************************************************
skipping: no hosts matched

PLAY RECAP **************************************************************************************************************************************

bash-5.0# ansible-playbook -i hosts sample.yml

PLAY [This is to make sure connectivity is working] *********************************************************************************************

TASK [Hostname display] *************************************************************************************************************************
changed: [vnflcm]

PLAY RECAP **************************************************************************************************************************************
vnflcm                     : ok=1    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
bash-5.0# cat hosts
vnflcm ansible_host=192.168.12.11 ansible_user=cloud-user ansible_password=today123
bash-5.0# cat sample.yml
---
- name: This is to make sure connectivity is working
  hosts: all
  gather_facts: false
  vars:
    ansible_command_timeout: 120
  any_errors_fatal: true
  max_fail_percentage: 0
  tasks:

    - name: Hostname display
      shell: hostname
```

Note: Always use ctrl+p+q to get out of the container    
