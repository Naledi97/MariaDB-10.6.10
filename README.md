//

MariaDB [(none)]> CREATE DATABASE ndjulu;
Query OK, 1 row affected (0.004 sec)

MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| ndjulu             |
| performance_schema |
| sys                |
+--------------------+
5 rows in set (0.003 sec)

//

MariaDB [(none)]> use ndjulu;
Database changed
MariaDB [ndjulu]> create user 'user_[ndjulu]'@localhost IDENTIFIED BY 'Naledi;';
Query OK, 0 rows affected (0.057 sec)

MariaDB [ndjulu]> Select user FROM mysql.user;
+---------------+
| User          |
+---------------+
| root          |
| root          |
| root          |
| root          |
| mariadb.sys   |
| root          |
| user_[ndjulu] |
+---------------+
7 rows in set (0.012 sec)

//
MariaDB [ndjulu]> GRANT ALL PRIVILEGES ON  *.* TO 'user_[ndjulu]'@localhost IDENTIFIED BY 'Naledi';
Query OK, 0 rows affected (0.065 sec)

MariaDB [ndjulu]> GRANT ALL PRIVILEGES ON ndjulu.* TO 'user_[ndjulu]'@localhost;
Query OK, 0 rows affected (0.062 sec)
