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


````
YAML -> Yet another markup language (DTO - Data Transfer objects)
````

