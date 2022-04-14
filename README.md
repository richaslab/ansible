# ansible

Installing Ansible

Check if Ansible already exists:

$ ansible --version

Ubuntu:
  $ sudo apt-get update

Next, install Ansible. Here are the steps to make that happen:

Log into the Ubuntu Server that will host Ansible
Install the necessary repository with the command 
  $ sudo apt-add-repository ppa:ansible/ansible

Update apt with the command sudo apt-get update.
Install Ansible with the command 
  $ sudo apt-get install ansible -y

Because Ansible requires a Python interpreter (in order to run its modules), we need to install Python as well. For that, issue the command:
  $ sudo apt-get install python -y
  
CONFIGURATION SETTINGS ON SERVER FOR PASSWORD LESS LOGIN TO HOST SERVER FOR ANSIBLE
------------------------------------------------------------------------------------
1. Create a new User for ansible administration and grant admin access to user(both control and managed node/server)
  $ useradd ansadm
  $ passwd ansadm
2. Provide Sudo access to new user
  $ visudo
  Go To Line: ## READ DROP IN FILES FROM /ETC/SUDOERS.D
  
  Check if winrm is open for Windows
  ___________________________________________
  
  winrm enumerate winrm/config/Listener
