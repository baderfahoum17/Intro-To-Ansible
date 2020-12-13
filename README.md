# Intro-To-Ansible

## Getting my Dirty with Ansible - 
### first hands on experince

this repo is mainly to document my first experince with Ansible 



---
the Basics: 

##### Why?:
As a DevOps or Someone who work in IT.
There will probably be a lot of repetitive tasks in our environment such as:
> 1. Creating new hosts or virtual machines everyday
> 2. applying new configuration on those machines 
>3. patching on a dozen of servers
>4. there will be a time when we will have to migrate from one version to a new one
>5. deploying applications
>6. one that is overlooked usualy: performing securit compliance audits

^^
these tasks involve execution of hundereds of commands on hundereds of different servers


> we can automate these tasks with scripts but those scripts require regular maintance and alot of time to put them together

**ANSIBLE** to the rescue!
Ansible is a powerfull IT automation tool that can help with the automation even of the most complex of deployments with relative ease with only a few lines of instructions in an ==ansible automation playbook==

...

this repo will demo a creation of a LAB environment via VirtualBox
in order to deomnstrate some of Ansible powerful capabilites 

we will be creating a Template of a OS to create 3 virtual machines 
One as a Ansible control Machine
Two other machines to taget for configuration changes

 ![Map](https://github.com/baderfahoum17/Intro-To-Ansible/blob/main/Screen%20Shot%202020-12-11%20at%2020.15.17.png)


... UNDER CONSTRUCTION

DOWNLOADS:
> we can download a costum image of CentOS from osboxes.org

> download VirutalBox from virtualbox.org

> we will be using an SSH Client either Mobaxtrem or Putty

INSTALLATION: 
> create a centOS template in virtualbox

> below attached image of the system snapshot

> use this template to create three virtual machines, Ansible-controller, ansible-target1, ansible-target2

> inside the virtualboxes run(foreach) `ifconfig` to extract the vm's ip address

> with our SSH client connect to those vm(it will be easier and faster to use the CLI rather than the vm GUI)

![snapshot](https://github.com/baderfahoum17/Intro-To-Ansible/blob/main/Screen%20Shot%202020-12-13%20at%2015.02.26.png)

> install ANSIBLE on the Ansible-controller machine `sudo yum install ansible`
(we do not need to install ansible on the target hosts because ansible is AGENTLESS, meaning no additional installation is needed on target hosts, as it uses SSH to establish a connection for its needs)
