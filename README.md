# loginsystem
Beléptető rendszer
## superuser
mysql -u root -p
SELECT User FROM mysql.user;
CREATE USER 'superuser'@'localhost' IDENTIFIED BY 'Passw0rd';
SELECT User FROM mysql.user;
GRANT ALL PRIVILEGES ON *.* TO 'superuser'@'localhost' WITH GRANT OPTION;
FLUSH PRIVILEGES;

-------------------------------------------------------------------------------
loginsystem user+database

CREATE DATABASE loginsystem_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
CREATE USER 'loginsystem'@'localhost' IDENTIFIED BY 'Passw0rd2026!';
GRANT ALL PRIVILEGES ON loginsystem_db.* TO 'loginsystem'@'localhost';
FLUSH PRIVILEGES;

SHOW DATABASES;
SELECT User, Host FROM mysql.user;
SHOW GRANTS FOR 'loginsystem'@'localhost';

mysql -u loginsystem -p loginsystem_db < users.sql

EXIT;
SELECT User, Host FROM mysql.user;
SHOW GRANTS FOR 'joomlauser'@'localhost';
EXIT;
