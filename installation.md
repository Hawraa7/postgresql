sudo apt update
sudo apt install -y postgresql postgresql-contrib
sudo service postgresql start
sudo -i
passwd gitpod
7Hussein25
7Hussein25
exit
sudo -i
visudo
gitpod ALL=(postgres) NOPASSWD: /usr/bin/psql
(Ctrl + X, then Y to confirm, and Enter)
exit
sudo -u postgres psql

# SQL Commands #
CREATE DATABASE chinook;
\l 
\c chinook
\i Chinook_PostgreSql.sql
SELECT * FROM "Artist";