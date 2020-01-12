### **Install H2 Databse**
Go to [H2 db download page](http://www.h2database.com/html/download.html) to download the newest version. I recommend you to download the platform independent zip file which can run in all windows, linux and macos.

Unzip the downloaded zip file to a local folder,
and go into the **bin** folder of unzipped h2 database

### **Create Database and User**
Run the below command to create new databse called **testdb** with user **user1**
######  java -cp h2-1.4.200.jar org.h2.tools.Script -url "jdbc:h2:~/.h2/testdb/testdb" -user "user1" -script "~/.h2/testdb/testdb_backup.sql"


Above command creates ```testdb``` in folder ```.h2/testdb``` of users home directory.

### **Open H2 Console**

Run the below command to open H2 Console ```java -jar h2-1.4.200.jar```

### **Connecting to H2 database from spring bot application**

Use the below properties to connecto to created h2 database

```spring.datasource.url=jdbc:h2:~/.h2/testdb/testdb;AUTO_SERVER=TRUE
spring.datasource.driverClassName=org.h2.Driver
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.H2Dialect

spring.datasource.username = user1
spring.datasource.password =

spring.h2.console.enabled=true
spring.jpa.hibernate.ddl-auto=create
spring.jpa.show-sql=true```