# hw12-backup

- Разворачиваем инфраструктуру в Vagrant

```
vagrant up
```
- Ждем некоторое время, и получаем бекапы

#### list job

```
[root@bacula-server backup]# echo "list jobs" | bconsole
Connecting to Director localhost:9101
1000 OK: bacula-dir Version: 5.2.13 (19 February 2013)
Enter a period to cancel a command.
list jobs
Automatically selected Catalog: MyCatalog
Using Catalog "MyCatalog"
+-------+---------------+---------------------+------+-------+----------+------------+-----------+
| jobid | name          | starttime           | type | level | jobfiles | jobbytes   | jobstatus |
+-------+---------------+---------------------+------+-------+----------+------------+-----------+
|     1 | BackupClient1 | 2019-03-28 21:57:12 | B    | F     |    2,400 | 27,197,685 | T         |
|     2 | BackupClient1 | 2019-03-28 22:05:02 | B    | D     |        0 |          0 | T         |
|     3 | BackupClient1 | 2019-03-28 22:07:02 | B    | I     |        0 |          0 | T         |
|     4 | BackupClient1 | 2019-03-28 22:17:02 | B    | I     |        0 |          0 | T         |
|     5 | BackupClient1 | 2019-03-28 22:27:02 | B    | I     |        0 |          0 | T         |
|     6 | BackupClient1 | 2019-03-28 22:35:02 | B    | D     |        0 |          0 | T         |
|     7 | BackupClient1 | 2019-03-28 22:37:02 | B    | I     |        0 |          0 | T         |
|     8 | BackupClient1 | 2019-03-28 22:47:02 | B    | I     |        0 |          0 | T         |
|     9 | BackupClient1 | 2019-03-28 22:57:02 | B    | I     |        0 |          0 | T         |
|    10 | BackupClient1 | 2019-03-28 23:05:02 | B    | D     |        0 |          0 | T         |
|    11 | BackupClient1 | 2019-03-28 23:07:02 | B    | I     |        0 |          0 | T         |
|    12 | BackupClient1 | 2019-03-28 23:17:02 | B    | I     |        0 |          0 | T         |
|    13 | BackupClient1 | 2019-03-28 23:27:02 | B    | I     |        0 |          0 | T         |
|    14 | BackupClient1 | 2019-03-28 23:35:02 | B    | D     |        0 |          0 | T         |
|    15 | BackupClient1 | 2019-03-28 23:37:02 | B    | I     |        0 |          0 | T         |
|    16 | BackupClient1 | 2019-03-28 23:47:02 | B    | I     |        0 |          0 | T         |
|    17 | BackupClient1 | 2019-03-28 23:57:02 | B    | I     |        0 |          0 | T         |
|    18 | BackupClient1 | 2019-03-29 00:00:02 | B    | F     |    2,400 | 27,197,685 | T         |
|    19 | BackupClient1 | 2019-03-29 00:05:02 | B    | D     |        0 |          0 | T         |
|    20 | BackupClient1 | 2019-03-29 00:07:03 | B    | I     |        0 |          0 | T         |
|    21 | BackupClient1 | 2019-03-29 00:17:03 | B    | I     |        0 |          0 | T         |
|    22 | BackupClient1 | 2019-03-29 00:27:03 | B    | I     |        0 |          0 | T         |
|    23 | BackupClient1 | 2019-03-29 00:35:03 | B    | D     |        0 |          0 | T         |
|    24 | BackupClient1 | 2019-03-29 00:37:03 | B    | I     |        0 |          0 | T         |
|    25 | BackupClient1 | 2019-03-29 00:47:03 | B    | I     |        0 |          0 | T         |
|    26 | BackupClient1 | 2019-03-29 00:57:03 | B    | I     |        0 |          0 | T         |
|    27 | BackupClient1 | 2019-03-29 01:05:03 | B    | D     |        0 |          0 | T         |
|    28 | BackupClient1 | 2019-03-29 01:07:03 | B    | I     |        0 |          0 | T         |
|    29 | BackupClient1 | 2019-03-29 01:17:03 | B    | I     |        0 |          0 | T         |
|    30 | BackupClient1 | 2019-03-29 01:27:03 | B    | I     |        0 |          0 | T         |
|    31 | BackupClient1 | 2019-03-29 01:35:02 | B    | D     |        0 |          0 | T         |
|    32 | BackupClient1 | 2019-03-29 01:37:02 | B    | I     |        0 |          0 | T         |
|    33 | BackupClient1 | 2019-03-29 01:47:02 | B    | I     |        0 |          0 | T         |
|    34 | BackupClient1 | 2019-03-29 01:57:02 | B    | I     |        0 |          0 | T         |
|    35 | BackupClient1 | 2019-03-29 02:05:02 | B    | D     |        0 |          0 | T         |
|    36 | BackupClient1 | 2019-03-29 02:07:02 | B    | I     |        0 |          0 | T         |
|    37 | BackupClient1 | 2019-03-29 02:17:02 | B    | I     |        0 |          0 | T         |
|    38 | BackupClient1 | 2019-03-29 02:27:02 | B    | I     |        0 |          0 | T         |
|    39 | BackupClient1 | 2019-03-29 02:35:02 | B    | D     |        0 |          0 | T         |
|    40 | BackupClient1 | 2019-03-29 02:37:02 | B    | I     |        0 |          0 | T         |
|    41 | BackupClient1 | 2019-03-29 02:47:02 | B    | I     |        0 |          0 | T         |
|    42 | BackupClient1 | 2019-03-29 02:57:02 | B    | I     |        0 |          0 | T         |
|    43 | BackupClient1 | 2019-03-29 03:05:02 | B    | D     |        0 |          0 | T         |
|    44 | BackupClient1 | 2019-03-29 03:07:02 | B    | I     |        0 |          0 | T         |
|    45 | BackupClient1 | 2019-03-29 03:17:02 | B    | I     |        0 |          0 | T         |
|    46 | BackupClient1 | 2019-03-29 03:27:02 | B    | I     |        0 |          0 | T         |
+-------+---------------+---------------------+------+-------+----------+------------+-----------+
You have messages.
You have mail in /var/spool/mail/root
```

#### list file

Результат команды `echo "list files jobid=1" | bconsole` в файле **jobid_1**
