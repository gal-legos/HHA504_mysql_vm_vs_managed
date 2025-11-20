# VM Setup Notes

## 1. VM Provisioning
- Cloud provider: GCP  
- Region: us-central1 (Iowa) 
    - Zone: us-central1-a
<img src="/screenshots/vm_demo/machine_setup1.png" alt="machine_setup_vm" width="350">


- Machine Size: e2-micro (2 vCPU, 1 core, 1 GB memory)
<img src="/screenshots/vm_demo/machine_setup.png" alt="machine_2_setup_vm" width="350">


- Image (Ubuntu xx.xx): Ubuntu 24.04 LTS Minimal 
<img src="/screenshots/vm_demo/os_setup_sc.png" alt="os_vm" width="350">


- Allow HTTP and HTTPS from networking rules 
<img src="/screenshots/vm_demo/network_rules_vm.png" alt="network_rules_1" width="350">

###### This will be done during the creation of the Virtual machine and lives in the 'Networking' tab on the left sandwiched between 'Data Protection' and 'Observability'. This is the networking rules after the VM was launched but very easy to find and change if needed. 

- Finished/running Virtual Machine 
<img src="screenshots/vm_demo/vm_running.png" alt="running" width="350">



## 2. Firewall / Security Group
- Allowed inbound 22, 3306
- Notes: Make sure to create a firewall rule and not a firewall policy when using GCP. 
<img src="/screenshots/vm_demo/firewall_rule.png" alt="firewall_vm" width="350">
<img src="/screenshots/vm_demo/security_access.png" alt="security_vm" width="350">
<img src="/screenshots/vm_demo/ip_filter_vm.png" alt="ip_filters_vm" width="350">
<img src="/screenshots/vm_demo/vm_network_name.png" alt="networks_vm" width="350">
<img src="/screenshots/vm_demo/ports_allowed.png" alt="ports_vm" width="350">



## 3. Commands Used Within the SSH Terminal 
sudo apt update

<img src="/screenshots/vm_demo/sudo_update.png" alt="update_vm" width="350">

###### Updates the SSH operating system 



sudo apt install mysql-server mysql-client nano -y

<img src="/screenshots/vm_demo/install_sql_nano.png" alt="install_vm" width="350">

###### Used to install packages into the SSH terminal that will be used for the assingment. Nano was included in this installation to troubleshoot a previous configuration issue that I ran into



sudo systemctl status mysql

<img src="/screenshots/vm_demo/system_check.png" alt="systemcheck_vm" width="350">

###### Using this command allows us to know if our sql server is active within the SSH Terminal 



sudo systemctl restart mysql 

<img src="/screenshots/vm_demo/system_check.png" alt="restart_sql" width="350">

###### Use this to restart mysql (NOTE: use this after changinf the bind address to 0.0.0.0)



mysql --version 

<img src="/screenshots/vm_demo/sql_version_check.png" alt="version_vm" width="350">

###### Used to find what version of sql we are running in the terminal



mysql -u 'user' -p 

<img src="/screenshots/vm_demo/testing_connection.png" alt="test_post_restart_vm" width="350">

###### Tests the connection using our user and pasword combination (NOTE: run this command after you finish setting up your SQL server with since this requires a user and password)



SQL QUERY: CREATE DATABASE
'CREATE DATABASE test_db'

<img src="/screenshots/vm_demo/dba_creation.png" alt="database_create_vm" width="350">

###### Used to create a specific database 

SQL QUERY: CREATE USER 
'CREATE USER 'user'@'%' IDENTIFIED BY 'StrongPass123!';'

<img src="/screenshots/vm_demo/create_user_vm.png" alt="create_user_vm" width="350">

###### Used to create a new user



SQL QUERY: GRANT
'GRANT ALL PRIVILEGES ON *.* TO 'user'@'%' WITH GRANT OPTION;'

<img src="/screenshots/vm_demo/grants_ssh_vm.png" alt="grant_user_vm" width="350">

###### used to grant access to users 



SQL query: SHOW DATABASES

<img src="/screenshots/vm_demo/show_databases_vm.png" alt="database_show_vm" width="350">

###### Shows all the databases that live in the sql server



## 4. Config files edited
/etc/mysql/mysql.conf.d/mysqld.cnf
- bind-address = 0.0.0.0


## 5. Python Script Output 
<img src="/screenshots/vm_demo/vm_demo_script_output.png" alt="output_vm" width="350">



## 6. Issues encountered
- Originally, I ran into an issue when attempting to change the bind-address. The SSH terminal would not recognize my sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf command, and told me it couldn't run the command. The issue had to be resolved by ensuring the security rules allowed access to all cloud APIs. There were some admin issues not recognizing my command, but changing the security access and then restarting the terminal fixed my problem, and I was able to change the bind address to 0.0.0.0
<img src="/screenshots/vm_demo/error.png" alt="error_vm" width="350">



## 7. Time to complete (minutes)
If everything ran properly the first time around, I would say it took about 5 minutes to set up the Virtual Machine (VM). To update and set up the SSH terminal for a connection with a Python script, it took about 10 minutes. The most time-consuming steps are updating and installing SQL on the OS. In total, it took me about 15 minutes with no issues; with issues, it was definitely longer than 15 minutes.
