# Docker testwork project for Telegraf, InfluxDB, Grafana and PostgreSQL stack.

## requirements 
- Ansible version 2.9.6
- SSH root connection to host

## in the hosts.txt add a hostname

```
linux1 ansible_host=192.168.2.240
```

## upd env to your dir with download project like this

```
compose_project_dir: "/home/ubuntu/docker-testwork/"
```

## cd to dir with project

```bash
$ cd /home/ubuntu/docker-testwork/
```

## Start the stack

```bash
$ ansible-playbook docker-testwork.yml -K
```

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

## in this project three dashboards for Grafana 

### 1. InfluxDB Docker - to monitoring 5 containers

![Example Screenshot](./1.png?raw=true "Example Screenshot")

### 2. Monitoring PostgreSQL Server

![Example Screenshot](./2.png?raw=true "Example Screenshot")

### 3. Telegraf-system-postgresql - monitoring local system parameters

![Example Screenshot](./3.png?raw=true "Example Screenshot")

## To see connections in PostgreSQL u can login in pgadmin make some server and take info in PostgreSQL dashboard 
