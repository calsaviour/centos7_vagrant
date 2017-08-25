## Objective
- This playbook will setup kafka and zookeeper in the vApp of a virtual data center (Vdc) or vSphere

## Prerequisite on vSphere Setup
- Setup the host VMs in the vApp or host vm in the vSphere
- Change the zone of firewall to public
- Change the inteface to public zone
- generate the ssh private and public key. Eg: ssh-keygen -t rsa
- copy the public keys to the kafka vm and zookeeper vm. Eg: ssh-copy-id user@123.45.56.78
- run the command ansible -m ping all -i hosts
- change the ip hosts group in the hosts file to match the relevant zookeeper and kafka setup


## Install dependencies
Run following commands to install ansible dependencies
ansible-galaxy install geerlingguy.java

## Objective:
This script will do the main following setup

run the ansible-playbook -i hosts site.yml

	### Kafka Setup
	1. yum install kafka
	2. open the following port 7203/tcp, 9092/tcp
	3. Add zookeeper connection to the server.properties file
	4. Configure it broker.id is the server.properties file

	### Zookeeper Setup
	1. yum install kafka (kafka rpm wil detect zookeeper as a dependency)
	2. open the following port 3888/tcp, 2181/tcp, 2888/tcp
	3. Add file /var/lib/zookeeper/myid
	4. Give a unique id in the file myid