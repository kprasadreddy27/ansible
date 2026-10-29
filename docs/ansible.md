# ansible

Install ansible 

```
sudo dnf install ansible -y
```

```
inventory -> list of items
```
```
Linux command === Ansible module/collection
```

ansible adhoc command  -> emergency purpose targeting one time simple task

Below are the ansible adhoc command 

```
ansible all -i <private ip of another server>, -e ansible_user=ec2-user -e ansible_password=DevOps321 -b -m dnf -a "name=nginx state=installed" -> to install

ansible all -i <private ip of another server>, -e ansible_user=ec2-user -e ansible_password=DevOps321 -b -m service -a "name=nginx state=started" -> to start
```


```
YAML -> Yet another markup language (DTO - Data Transfer objects)
```

Install (nginx) on another server using playbook

```
ansible-playbook -i inventory.ini -e ansible_username=ec2-user -e ansible_password=DevOps321 04-playbook.yaml
```

To provide cmd variables

```
ansible-playbook -i inventory.ini 09-variables.yaml -e "person_name=prasad"
```

Variables preference:

```
CMD
task
File
prompt
Play
Inventory
```

In Ansible

```
variables == facts  (01-gather-facts.yaml)
```


Ansible configuration
```
In ansible installed server

cd
ansible --version
cat /etc/ansible/ansible.cfg
To generate example config file , we have cmd in above file.

mkdir ansible-test
cd ansible-test
vi ansible.cfg
copy content which are taken from generated example config file

export ANSIBLE_CONFIG=/home/ec2-user/ansible-test/ansible.cfg

ansible --version
```

To unset default
```
unset ANSIBLE_CONFIG
then check ansible --version
```

Ansible configuration priority

```
configurations in /etc
default -> /etc/ansible/ansible.cfg

1. ANSIBLE_CONFIG env variable
2. current working directory
3. home directory with .ansible.cfg
4. /etc/ansible/ansible.cfg




