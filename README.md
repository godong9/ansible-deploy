# ansible-deploy
Ansible deploy project

# Install ansible
```
$ brew install ansible
```

# Server setup (Ubuntu)
```
$ ansible-playbook -i inventories/{{stage}} server_setup.yml
```

# Java setup
```
$ sudo add-apt-repository ppa:webupd8team/java
$ sudo apt update; sudo apt install oracle-java8-installer
$ sudo apt install oracle-java8-set-default
```


## 참고
[Ansible Best Practices](http://docs.ansible.com/ansible/playbooks_best_practices.html)
[Ansible Examples](https://github.com/ansible/ansible-examples)