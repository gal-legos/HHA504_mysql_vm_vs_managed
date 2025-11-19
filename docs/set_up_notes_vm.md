# VM Setup Notes

## 1. VM Provisioning
- Cloud provider:
- Region:
- Instance size:
- Image (Ubuntu xx.xx):

## 2. Commands Used
sudo apt update
sudo apt install mysql-server -y
sudo systemctl enable mysql
sudo systemctl status mysql

## 3. Config files edited
/etc/mysql/mysql.conf.d/mysqld.cnf
- bind-address = 0.0.0.0

## 4. Firewall / Security Group
- Allowed inbound 22, 3306
- Notes:

## 5. Issues encountered
- 
- 

## 6. Time to complete (minutes)
