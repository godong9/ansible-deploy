# ansible-deploy
Ansible deploy project

# Install ansible
```
$ brew install ansible
```

# Add deploy user
```
$ sudo adduser deploy
$ sudo visudo

    deploy ALL=(ALL:ALL) ALL
```

# Server setup (Ubuntu)
```
$ ansible-playbook -i inventories/{{stage}} server_setup.yml
```

# Java setup (실행 X -> devel.yml에 포함됨)
```
$ sudo add-apt-repository ppa:webupd8team/java
$ sudo apt update; sudo apt install oracle-java8-installer
$ sudo apt install oracle-java8-set-default
```

# Nginx service
```
$ ansible-playbook -i inventories/{{stage}} nginx_service.yml -e start=true
```

# Board 배포
```
$ ansible-playbook -i inventories/{{stage}} board_deploy.yml
```

## 참고
[Ansible Best Practices](http://docs.ansible.com/ansible/playbooks_best_practices.html)
[Ansible Examples](https://github.com/ansible/ansible-examples)