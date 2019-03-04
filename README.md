# The Worlds Most Affordable Web Server
In this lab we will be leveraging the power of Ansible to configure a Raspberry Pi Zero W to be a web server and deploy a React app! Today you make your own destiny, you have the application, you have the infrastructure, and you have a dream. Lets make it happen!

## Prerequisites
* Raspberry Pi Zero W
* Python 3
* Ansible Installed

## Install Ansible
### Mac OSX
```
sudo pip install ansible
```
For issues reference [this](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#latest-releases-via-pip) guide 

### Linux/Ubuntu
```
sudo apt-get update
sudo apt-get install software-properties-common
sudo apt-add-repository --yes --update ppa:ansible/ansible
sudo apt-get install ansible
```

### RHEL/Centos/Fedora
```
rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
sudo yum install ansible
```

### Windows
```
This is outside the scope of this lab... talk to me about getting a clound instance to work from.
```

## Getting Started
Begin by writing your inventory file. Hint: find your ip address on your server using `hostname -I`

Note: The username for your raspberry pi is: **pi** the password is: **raspberry** this may be
important for running your ansible playbook _wink_ _wink_

## Your Goal:
Deploy a website on an Raspberry Pi Zero W or a server of your choice. To do so:
* **install** an apache http web server and firewall daemon **(packages: apache2, apache2-utils, firewalld)** 
* Start the http **apache2** and **firewalld** services and enable them at start up
* Create a firewall exception for the http service that takes effect right away and persists after reboot
* Write a index.html file to the /var/www/html/ directory with anythin you like inside

## Bonus:
### Level 1:
Make your play book idempotent, that means your playbook changes nothing after the first time you run it.

### Level 2: 
Leverage variables in your playbook for either service names, package names, or paths

### Level 3:
Deploy your hackathon application to the apache web server to demo to judges using Ansible

## Author
* Griffin College - [Red Hat](https://www.redhat.com/en)

## License
This project rocks an MIT License

