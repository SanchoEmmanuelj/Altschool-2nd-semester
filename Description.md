The files in this repository will enable us:

- Provision a Master and Slave Ubuntu based Servers.(SEE CODE IN THE BASHSCRIPT DIRECTORY NAMED master-slave.sh)

- Deploy LAMP (Linux, Apache, MySQL, PHP) stack
  
  a) This script also Clones PHP Laravel and its dependensies (SEE BASH SCRIPT IN THE BashScript DIRECTORY NAMED laravelBash-script.sh)

- Ansible playbook that automates the deployment of PHP.


SCRIPTS INCLUDE 

1) master-slave.sh ( this will deploy the master and slave ubuntu based servers on virtual box, with 2 CPUs and 1GB of memory)



2) laravelBash-script.sh on the Master server this script will:
   - update and upgrade server 
   - install LAMP stack
   - Install Composer
   - configure Apache2
   - Clone Laravel and its Dependencies 
   - Configuring MySQL
   - configuring a Laravel project's database settings and running migrations for PHP

   NB: Run this script with sancho and sancho90 as database username and password respectively
  ![image1](<Laravel on Master.png>)
  ![image2](<Images/Laravel  with Master IP address.png>)

3) Ansible-playbook which contains 
  - inventory file with the slave server IP address (inventory)
  - ansible config file (ansible.cfg)
  - site.yaml script which is the Ansible playbook for configuring and managing a remote server.
  - files directory in which we have laravel script for the slave server 

  NB:the passphrase when you run the site.yaml is (sancho)
  - Running the ansible-playbook site.yaml produced this outcome
![image3](<Images/Slave ansible.png>)
![image4](<Images/Slave IP laravel.png>)
