# task3


Setup Ansible on AWS (Ubuntu server):-

Launch an instance from AWS launch wizard.
Make sure SSH port 22 is available on the security group.
Name your server as ‘Ansible_Master’ and connect to that machine.
Update packages by running the below command.
        $ apt update

If you install Ansible on Ubuntu it will install python, but anyways make sure whether python installed or not.
          $ apt install -y ansible

Check ansible and python is installed or not.
          $ which python

           $ which ansible

Ansible is not a service but it is a tool, so no need to start as a service.
When you install Ansible you’re going to get a folder called   ‘/etc/ansible’. Under this, there are two files.
/etc/ansible/ansible.cfg :- It is a configuration file here we are going to tell how ansible should be running.

/etc/ansible/hosts:-  whatever machines that we want Ansible to connect that information we are going to give in this file. It is a default file and we can change it later, it is called inventory file.

Goto /etc/ansible/ansible.cfg, here everything is commented so uncomment “inventory” and “sudo_user”.

 we have to give a machine name, it will be any name. (Node1)
Private IP of the machine and default user of that machine.
Copy the pem key file somewhere in the master machine and give that path.
Then try to connect those machines using the below command.
$ ansible -m ping all
$ ansible-playbook apache.yml

