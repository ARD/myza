# MYZA
Simple Bash Script for dump MySQL databases. This script depends on **mysqldump**


**Dump all databases widh compression**
```
./myza -u mysqlUser -p mysqlPassword -a -c -d /home/user/backup/
```


**Dump tables in separate files**
```
./myza -u mysqlUser -p mysqlPassword -a -c -t -d /home/user/backup/
```


**Dump only one database with gzip compression and one table per file**
```
./myza -u mysqlUser -p mysqlPassword -l "my_database_name" -c -t -d /home/user/backup/
```

**USAGE**

Parameter    | Description
------------ | -------------
-h, --help | show this help text
-u | set database username
-p | set database password
-l | list of databases for dump
-a | dump all databases
-c | compress dump file with gzip
-t | dump tables in separate files
-d | define directory path for dump files
-v, --verbose | print info about dump process
