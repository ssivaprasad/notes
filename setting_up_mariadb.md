### **Setting Up Maria DB**

1. Goto Unzipped folder of Mariadb

2. Goto **bin** folder

3. mysql_install_db.exe --datadir=..\data              &emsp; **// Install Sample Schema and Point to data directory**

4. mysqld --console                                    &emsp;	**// Should run and ready for connections**

5. mysql -h localhost -u root					 &emsp; 	**// Open another Terminal and run this command**

6. alter user 'root'@'localhost' identified by 'root';  	&emsp; **// change default password for root**

7. mysql -h localhost -u root -p                        &emsp; **// Try to login with updated root user password**

   &emsp; mysql_install_db.exe --datadir=..\data --pasword=test123	&emsp; **// Another way to change root password**

8. show databases;

9. create database hibernatedb;

10. drop database hibernatedb;


SET GLOBAL time_zone = '+3:00';

**Create User and give permission to sepcific databse***

create user 'hibernate'@'localhost' identified by 'hibernate';

grant  all privileges ON hibernatedb.* TO 'hibernate'@'localhost' IDENTIFIED BY 'hibernate';

**Create another root user**

create user 'admin'@'localhost' identified by 'admin';

GRANT ALL PRIVILEGES ON *.* TO 'admin'@localhost IDENTIFIED BY 'admin';

FLUSH PRIVILEGES;



*******
MYSQL
*******
create user 'mysql'@'localhost' identified by 'mysql';

GRANT ALL PRIVILEGES ON *.* TO 'mysql'@'localhost' WITH GRANT OPTION;

FLUSH PRIVILEGES;



https://phoenixnap.com/kb/how-to-create-mariadb-user-grant-privileges
