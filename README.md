### If you are working on Aws 
###### Make sure that you are picking the AMI ID's as specified below.
```
ap-northeast-1 = "ami-0567c164"
ap-southeast-1 = "ami-a1288ec2"
cn-north-1 = "ami-d9f226b4"
eu-central-1 = "ami-8504fdea"
eu-west-1 = "ami-0d77397e"
sa-east-1 = "ami-e93da085"
us-east-1 = "ami-40d28157"
us-west-1 = "ami-6e165d0e"
us-west-2 = "ami-a9d276c9"
```
### Installing K8S using ansible 

##### Prerequisite 
Luanch one server and install the ansible & git as below
###### Ubuntu
```
apt-add-repository ppa:ansible/ansible
apt-get update
apt-get  install ansible -y
```
```
If you are facing below issue then please follow the instructions as specified below

root@ip-172-31-16-231:~# apt-add-repository ppa:ansible/ansible
Cannot add PPA: 'ppa:~ansible/ubuntu/ansible'.
ERROR: '~ansible' user or team does not exist.
```
###### Solution
```
apt-get update -y
apt-get upgrade -y
apt-add-repository ppa:ansible/ansible
apt-get update
apt-get  install ansible -y
root@ip-172-31-16-231:~# ansible --version
ansible 2.9.27
Note: Make sure that your ansible version is latest
```

###### Centos
```
yum install epel-release ansible -y
```
###### Amazon Linux
```
sudo amazon-linux-extras install epel -y
sudo yum install ansible -y
```
