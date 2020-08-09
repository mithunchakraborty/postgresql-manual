# PostreSQL Manual
Just quick instructions for the Postgresql
### Table of Contents
- [Installing](#installation-from-source)
## Installation from source
1. Downloading source from repository
```bash
cd ~/Desktop
wget https://ftp.postgresql.org/pub/source/v12.3/postgresql-12.3.tar.gz
```
2. Unzip archive and go to the directory
```bash
tar -xzvf postgresql-12.3.tar.gz
cd postgresql-12.3
```
3. Configure
```bash
./configure --prefix=/var/lib/postgresql
```
4. Make with extensions
```bash
make world
```
5. Install
```bash
sudo make install-world
```
6. Make the postgres folder owner
```bash
sudo chown -R mithun /var/lib/postgresql
```
7. Create PGDATA
```bash
export PGDATA=/var/lib/postgresql/main
```
8. Creating a data cluster
```bash
cd /var/lib/postgresql
./bin/pg_ctl initdb
```
9. Starting the database server
```bash
./bin/pg_ctl -l logfile -D /var/lib/postgresql/main/ start
```
10. Creating a database
```bash
./bin/psql -h localhost -U mithun postgres
create database some_db;
\c some_db
```
11. Removing sources
```bash
cd ~/Desktop
rm -rf postgresql-12.3.tar.gz postgresql-12.3
```

