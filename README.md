# HHA504 MySQL VM vs Managed Service


## Assignment Overview
This assignment provides an opportunity to compare the process of running a MySQL server using both a Managed Service and a Virtual Machine (VM) within the Google Cloud Platform. Each environment required the use of Pandas, SQLAlchemy, and Python to create databases, define tables, and execute scripts, allowing for a structured evaluation of their differences in setup, functionality, and overall usability.



## Cloud Provider
GCP console (Google Cloud Platform)
Both the VM and Managed Service were in the us-central1 (Iowa) region with the VM specifically being in the us-central1-a zone


## Steps to Reproduce Managed Service
- Create a MySQL instance in Cloud SQL
   - Create the lowest cost server by customizing
   <img src="/screenshots/managed_demo/cost_managed.png" alt="cost" width="300">
- Create a User and a password needed for the Python script
- Create a database with the SQL Editor
- Grant user access
- Put secrets into a hidden `.env`
- Create a virtual environment to run Python packages and scripts
- Run scripts:
 - python scripts/managed_demo.py


##### Supporting screenshots and step information can be found in the /docs/set_up_notes_managed file


## Steps to Reproduce Virtual Machine Instance
- Create VM
- Open firewall for 3306
- Open the SSH Terminal
- Run updates and install MySQL
- Configure bind-address
- Create Managed MySQL
   - Create a user and a database
   - Grant access
- Test Connection
- Put secrets into a hidden `.env`
- Create a virtual environment to run Python packages and scripts
- Run scripts:
 - python scripts/vm_demo.py


##### Supporting screenshots and step information can be found in the /docs/set_up_notes_vm file


## Connection String Pattern
mysql+pymysql://USER:PASS@HOST:PORT/DBNAME
(no secrets included)


## Screenshots
Screenshots can be found in their respective files under the 'screenshots' folder and in the setup notes for each of the GCP systems. 

## Video Repo Tour and Script Run
Video Link (https://www.loom.com/share/64813ed0095f4bea8428bf0336dbcb0c)

