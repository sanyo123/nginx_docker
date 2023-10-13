# Ansible


### installing ansible on ubuntu:
```
Open terminal and run:

sudo apt-add-repository ppa:ansible/ansible

sudo apt update

sudo apt install ansible
```
#### 1. Add host to host.ini

```
add host in host.ini:
[ec2] ## this is name of host
IP ansible_port=22 ansible_ssh_private_key_file=path to your key ansible_user=ubuntu
-- example --:
[ec2] ## this is name of host
52.73.224.136 ansible_port=22 ansible_ssh_private_key_file=/home/user/.ssh/yourkey.pem ansible_user=ubuntu

After that go in folder where is your host.ini located with terminal cd myfolder and run:
ansible ec2 -i host.ini -m ping

if ping is okay you are connected to ec2 instance:

 52.73.224.136 SUCCESS =>

```
#### 2.Run ansible setup.yml
```
Go in folder where is your where is your setup.yml, cd myfolder in terminal , and run this command with terminal :

ansible-playbook -i host.ini setup.yml
```
