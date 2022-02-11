# My-Sql-Excercises
show databases;

+--------------------+
| Database           |
+--------------------+
| assesment          |
| information_schema |
| mysql              |
| performance_schema |
| sakila             |
| sys                |
| userdata           |
| world              |
+--------------------+
8 rows in set (0.01 sec)
Enter password: ********
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 11
Server version: 8.0.28 MySQL Community Server - GPL

Copyright (c) 2000, 2022, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| assesment          |
| information_schema |
| mysql              |
| performance_schema |
| sakila             |
| sys                |
| userdata           |
| world              |
+--------------------+
8 rows in set (0.01 sec)

mysql> use userdata;
Database changed
mysql> create table userdata;
ERROR 4028 (HY000): A table must have at least one visible column.
mysql> show tables;
+--------------------+
| Tables_in_userdata |
+--------------------+
| blazers            |
| cars               |
| students           |
+--------------------+
3 rows in set (0.01 sec)

mysql> select * from studenst;
ERROR 1146 (42S02): Table 'userdata.studenst' doesn't exist
mysql> select * from students;
+----+-----------+--------+----------------+--------------------+-----+
| Id | username  | gender | city           | address            | age |
+----+-----------+--------+----------------+--------------------+-----+
|  1 | aswath    | male   | ramanathapuram | aliyar street      |  18 |
|  2 | kaushik   | male   | chennai        | velachery street   |  19 |
|  3 | haiden    | male   | tirunelveli    | koothankuli street |  19 |
|  4 | annamalai | male   | madurai        | othakadai          |  18 |
|  5 | santhanu  | male   | theni          | theni main road    |  19 |
|  6 | prasanna  | male   | thanjavur      | thanjavur street   |  21 |
|  7 | deepak    | male   | chennai        | omr main street    |  19 |
|  8 | musharaf  | male   | Ramanathapuram | rs mangalam        |  20 |
|  9 | rishi     | male   | tirupur        | tirupur            |  19 |
| 10 | venkat    | male   | tirunelveli    | tlv street         |  19 |
| 11 | riyas     | male   | thoothukudi    | tir street         |  18 |
| 12 | saranya   | female | tirunelveli    | tlv street         |  17 |
| 13 | abisha    | female | tirunelveli    | tlv street         |  18 |
| 14 | jerusheya | female | tirunelveli    | papanasam street   |  20 |
+----+-----------+--------+----------------+--------------------+-----+
14 rows in set (0.03 sec)

mysql> select * from students LIMIT 6,10;
+----+-----------+--------+----------------+------------------+-----+
| Id | username  | gender | city           | address          | age |
+----+-----------+--------+----------------+------------------+-----+
|  7 | deepak    | male   | chennai        | omr main street  |  19 |
|  8 | musharaf  | male   | Ramanathapuram | rs mangalam      |  20 |
|  9 | rishi     | male   | tirupur        | tirupur          |  19 |
| 10 | venkat    | male   | tirunelveli    | tlv street       |  19 |
| 11 | riyas     | male   | thoothukudi    | tir street       |  18 |
| 12 | saranya   | female | tirunelveli    | tlv street       |  17 |
| 13 | abisha    | female | tirunelveli    | tlv street       |  18 |
| 14 | jerusheya | female | tirunelveli    | papanasam street |  20 |
+----+-----------+--------+----------------+------------------+-----+
8 rows in set (0.00 sec)

mysql> https://github.com/ASWATH48/My-Sql-Excercises.git
    -> /c
    -> /c;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'https://github.com/ASWATH48/My-Sql-Excercises.git
/c
/c' at line 1
mysql> select * from students LIMIT 5,5;
+----+----------+--------+----------------+------------------+-----+
| Id | username | gender | city           | address          | age |
+----+----------+--------+----------------+------------------+-----+
|  6 | prasanna | male   | thanjavur      | thanjavur street |  21 |
|  7 | deepak   | male   | chennai        | omr main street  |  19 |
|  8 | musharaf | male   | Ramanathapuram | rs mangalam      |  20 |
|  9 | rishi    | male   | tirupur        | tirupur          |  19 |
| 10 | venkat   | male   | tirunelveli    | tlv street       |  19 |
+----+----------+--------+----------------+------------------+-----+
5 rows in set (0.00 sec)

mysql> select * from students order by id desc limit 0,1;
+----+-----------+--------+-------------+------------------+-----+
| Id | username  | gender | city        | address          | age |
+----+-----------+--------+-------------+------------------+-----+
| 14 | jerusheya | female | tirunelveli | papanasam street |  20 |
+----+-----------+--------+-------------+------------------+-----+
1 row in set (0.00 sec)

mysql> select max(age) from students;
+----------+
| max(age) |
+----------+
|       21 |
+----------+
1 row in set (0.01 sec)

mysql> select min(age) from students;
+----------+
| min(age) |
+----------+
|       17 |
+----------+
1 row in set (0.00 sec)

mysql> select avg(age) from students;
+----------+
| avg(age) |
+----------+
|  18.8571 |
+----------+
1 row in set (0.01 sec)

mysql> select round(avg(age)) from students;
+-----------------+
| round(avg(age)) |
+-----------------+
|              19 |
+-----------------+
1 row in set (0.01 sec)

mysql> select avg(age) from students;
+----------+
| avg(age) |
+----------+
|  18.8571 |
+----------+
1 row in set (0.00 sec)

mysql> select sum(age) from students;
+----------+
| sum(age) |
+----------+
|      264 |
+----------+
1 row in set (0.01 sec)

mysql> select city count(id) from students;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'count(id) from students' at line 1
mysql> select city count(id) group by city from students;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'count(id) group by city from students' at line 1
mysql> select city, count(id) group by city from students;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'from students' at line 1
mysql> select city, count(id)  from students;
+----------------+-----------+
| city           | count(id) |
+----------------+-----------+
| ramanathapuram |        14 |
+----------------+-----------+
1 row in set (0.00 sec)

mysql> select city, count(id) from students group by city;
+----------------+-----------+
| city           | count(id) |
+----------------+-----------+
| ramanathapuram |         2 |
| chennai        |         2 |
| tirunelveli    |         5 |
| madurai        |         1 |
| theni          |         1 |
| thanjavur      |         1 |
| tirupur        |         1 |
| thoothukudi    |         1 |
+----------------+-----------+
8 rows in set (0.01 sec)

mysql> select gender, count(id) from students group by gender;
+--------+-----------+
| gender | count(id) |
+--------+-----------+
| male   |        11 |
| female |         3 |
+--------+-----------+
2 rows in set (0.00 sec)

mysql> select gender, count(id) as no_of from students group by gender;
+--------+-------+
| gender | no_of |
+--------+-------+
| male   |    11 |
| female |     3 |
+--------+-------+
2 rows in set (0.00 sec)

mysql> select gender, count(id) as no_of_students from students group by gender;
+--------+----------------+
| gender | no_of_students |
+--------+----------------+
| male   |             11 |
| female |              3 |
+--------+----------------+
2 rows in set (0.00 sec)

mysql> select name, count(id) as no_of_students from students group by gender;
ERROR 1054 (42S22): Unknown column 'name' in 'field list'
mysql> select username, count(id) as no_of_students from students group by gender;
+----------+----------------+
| username | no_of_students |
+----------+----------------+
| aswath   |             11 |
| saranya  |              3 |
+----------+----------------+
2 rows in set (0.00 sec)

mysql> select username from students group by gender;
+----------+
| username |
+----------+
| aswath   |
| saranya  |
+----------+
2 rows in set (0.00 sec)

mysql> select username from students order by gender;
+-----------+
| username  |
+-----------+
| saranya   |
| abisha    |
| jerusheya |
| aswath    |
| kaushik   |
| haiden    |
| annamalai |
| santhanu  |
| prasanna  |
| deepak    |
| musharaf  |
| rishi     |
| venkat    |
| riyas     |
+-----------+
14 rows in set (0.01 sec)

mysql> select username from students where name like 'A%';
ERROR 1054 (42S22): Unknown column 'name' in 'where clause'
mysql> select username from students where username like 'A%';
+-----------+
| username  |
+-----------+
| aswath    |
| annamalai |
| abisha    |
+-----------+
3 rows in set (0.00 sec)

mysql> select username from students where username like '%YA';
+-----------+
| username  |
+-----------+
| saranya   |
| jerusheya |
+-----------+
2 rows in set (0.00 sec)

mysql> select username from students where username like '%A%';
+-----------+
| username  |
+-----------+
| aswath    |
| kaushik   |
| haiden    |
| annamalai |
| santhanu  |
| prasanna  |
| deepak    |
| musharaf  |
| venkat    |
| riyas     |
| saranya   |
| abisha    |
| jerusheya |
+-----------+
13 rows in set (0.00 sec)

mysql> select username from students where username like '%us%';
+-----------+
| username  |
+-----------+
| kaushik   |
| musharaf  |
| jerusheya |
+-----------+
3 rows in set (0.00 sec)

mysql> select  from students where city ='ramanathapuram' and city = 'tirunelveli';
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'from students where city ='ramanathapuram' and city = 'tirunelveli'' at line 1
mysql> select *  from students where city ='ramanathapuram' and city = 'tirunelveli';
Empty set (0.00 sec)

mysql> select *  from students where city ='ramanathapuram' or city = 'tirunelveli';
+----+-----------+--------+----------------+--------------------+-----+
| Id | username  | gender | city           | address            | age |
+----+-----------+--------+----------------+--------------------+-----+
|  1 | aswath    | male   | ramanathapuram | aliyar street      |  18 |
|  3 | haiden    | male   | tirunelveli    | koothankuli street |  19 |
|  8 | musharaf  | male   | Ramanathapuram | rs mangalam        |  20 |
| 10 | venkat    | male   | tirunelveli    | tlv street         |  19 |
| 12 | saranya   | female | tirunelveli    | tlv street         |  17 |
| 13 | abisha    | female | tirunelveli    | tlv street         |  18 |
| 14 | jerusheya | female | tirunelveli    | papanasam street   |  20 |
+----+-----------+--------+----------------+--------------------+-----+
7 rows in set (0.00 sec)

mysql> select *  from students where city in('ramanathapuram' ,  'tirunelveli');
+----+-----------+--------+----------------+--------------------+-----+
| Id | username  | gender | city           | address            | age |
+----+-----------+--------+----------------+--------------------+-----+
|  1 | aswath    | male   | ramanathapuram | aliyar street      |  18 |
|  3 | haiden    | male   | tirunelveli    | koothankuli street |  19 |
|  8 | musharaf  | male   | Ramanathapuram | rs mangalam        |  20 |
| 10 | venkat    | male   | tirunelveli    | tlv street         |  19 |
| 12 | saranya   | female | tirunelveli    | tlv street         |  17 |
| 13 | abisha    | female | tirunelveli    | tlv street         |  18 |
| 14 | jerusheya | female | tirunelveli    | papanasam street   |  20 |
+----+-----------+--------+----------------+--------------------+-----+
7 rows in set (0.00 sec)

mysql> select *  from students where city in('ramanathapuram' ,  'tirunelveli');
