# HHA504 MySQL VM vs Managed Service

## Cloud Provider
(e.g., Google Cloud, Region us-central1)

## Repo Structure
(brief list)

## Steps to Reproduce
- Create VM
- Install MySQL
- Configure bind-address
- Open firewall for 3306
- Create Managed MySQL
- Put secrets into `.env`
- Run scripts:
  - python scripts/vm_demo.py
  - python scripts/managed_demo.py

## Connection String Pattern
mysql+pymysql://USER:PASS@HOST:PORT/DBNAME
(no secrets included)

## Screenshots
See `screenshots/vm/` and `screenshots/managed/`

## Video Demo
(link to Loom/Zoom recording)
