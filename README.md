# Docker testwork project for Telegraf, InfluxDB, Grafana and PostgreSQL stack.

## requirements 
- Ansible version 2.9.6
- SSH root connection to host
- Ubuntu 20.04 on the remote host

## in the hosts.txt add a hostname

```
linux1 ansible_host=192.168.2.240
```

## upd env in the docker-testwork.yml playbook to your user on the remote host like this

```
user: "ubuntu"
```

## cd to dir with project

```bash
$ cd /home/ubuntu/docker-testwork/
```

## Start the stack

```bash
$ ansible-playbook docker-testwork.yml -K
```

## Grafana start
- go to hostname ip your remote host like http://192.168.2.240:3000
- login in the Grafana and change password
- On the main menu left go to Dashboards/Manage
- then u can see three dashboards, start use one of them

### 1. InfluxDB Docker - to monitoring 5 containers

![Example Screenshot](./1.png?raw=true "Example Screenshot")

### 2. Monitoring PostgreSQL Server

![Example Screenshot](./2.png?raw=true "Example Screenshot")

### 3. Telegraf-system-postgresql - monitoring local system parameters

![Example Screenshot](./3.png?raw=true "Example Screenshot")

## To see connections in PostgreSQL u can login in pgadmin make some server and take info in PostgreSQL dashboard 

## Credentials 

### Grafana
- Port: 3000 
- User: admin 
- Password: admin 

### Telegraf
- Port: 8125

### InfluxDB
- Port: 8086
- User: admin 
- Password: admin 
- Database: influx

### PostgreSQL
- Port: 5432
- User: postgres 
- Password: changeme 
- Database: postgres

### Pgadmin
- Port: 5050
- Password: admin 
- Database: postgres
