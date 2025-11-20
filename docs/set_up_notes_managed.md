# Managed MySQL Setup Notes

## 1. Service Details
- Engine version: GCP Cloud SQL
- Tier: Enterprise 
    - DB Version: MySQL 8.0
    - vCPU/RAM: 2vCPU/ 8 GB
<img src="/screenshots/managed_demo/enterprise_selection_setup.png" alt="engine_version" width="350">  
<img src="/screenshots/managed_demo/mysql_instance_info_setup.png" alt="instance_info" width="350"> 
<img src="/screenshots/managed_demo/machine_config_setup.png" alt="vcpu_info" width="350"> 


- Region: us-central1 (Iowa)
<img src="/screenshots/managed_demo/zones_setup.png" alt="zones_regions" width="350">


- Storage: 10 GB SSD
<img src="/screenshots/managed_demo/storage_setup.png" alt="storage" width="350">



## 2. Network Configuration
- Public IP allowlist: 0.0.0.0/0 (allows internet access)
- Authorized networks: 0.0.0.0/0 
<img src="/screenshots/managed_demo/security_setup.png" alt="security" width="350">
<img src="/screenshots/managed_demo/network_allows_setup.png" alt="network" width="350">
<img src="/screenshots/managed_demo/data_protection_setup.png" alt="data_protection" width="350">
<img src="/screenshots/managed_demo/connections_setup.png" alt="connections" width="350">



## 3. Completed Managed Service launch 
<img src="/screenshots/managed_demo/mysql_managed_finished.png" alt="finished" width="350">
<img src="/screenshots/managed_demo/connection_info_managed.png" alt="connection_info" width="350">

###### This is what it should look like when the managed service has been launched 



## 4. Initial Admin Setup
- Adding a User apart from Root User 
<img src="/screenshots/managed_demo/add_user_managed.png" alt="user" width="350">
<img src="/screenshots/managed_demo/user_managed.png" alt="user_1" width="350">


- Grant User Access with GCP SQL Studio  
<img src="/screenshots/managed_demo/grant_access_withsql.png" alt="grants" width="350">

###### Used the same SQL query as the VM set up to grant access


- Create Database with GCP SQL Studio
<img src="/screenshots/managed_demo/create_db_managed.png" alt="database" width="350">

###### Used the same SQL query as the VM set up to create a database



## 5. Python Script output 
<img src="/screenshots/managed_demo/vscode_managed_output.png" alt="python_output" width="350">



## 6. Time to complete (minutes):
In total, the time it took to create the Managed instance with Google's MySQL, I would estimate to be about 10 minutes. This includes creating the user and database using the tabs on the left side of the Cloud SQL navigation.


## 7. Issues encountered:
No issues encountered. However, I did not use the Google Cloud Shell at any point in this setup, so there may be an issue that could have appeared had I used the Cloud Shell instead of the Regular Cloud MySQL user interface. 
