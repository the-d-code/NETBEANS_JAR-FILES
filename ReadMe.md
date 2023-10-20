# 1) For All Property 

Payara_Server -> glassfish -> lib -> here place mysql-connector-java-5.0.8-bin.jar file

# 2) for pool connection

http://localhost:4848/common/index.jsf
==========================================================================================
from sidebar 
in Resources -> JDBC -> JDBC Connection Pools -> New
==========================================================================================
Pool Name : exam
Resource Type : javax.sql.DataSource
Database Driver Vendor : MySql
==========================================================================================
press Next
------------------------------------
<br/>in Additional Properties section

Add this two Proerties
-------------------------------------
<br/>**driver** : com.mysql.jdbc.Driver<br/>
<br/>**driverClass** : com.mysql.jdbc.Driver
<br/>
find this properties
-------------------------------------
<br/>**User** : PhpMyAdmin_Username
<br/>**Password** : PhpMyAdmin_Password
<br/>**ServerName** : localhost
<br/>**DatabaseName** : your_datbase_name
<br/>**URL** : jdbc:mysql://localhost:3306/your_datbase_name
<br/>URL : jdbc:mysql://localhost:3306/your_datbase_name
<br/>--------------------------------------
<br/>press Finish

# 3) for jndi

http://localhost:4848/common/index.jsf
<br/>---------------------------------------
from sidebar 
<br/>in Resources -> JDBC -> JDBC Resources -> New
<br/>---------------------------------------
<br/>JNDI Name : jdbc/exam // exam is pool name
<br/>Pool Name : exam
<br/>---------------------------------------
<br/>press OK

# 4) ping

http://localhost:4848/common/index.jsf
<br/>----------------------------------------
<br/>from sidebar 
<br/>in Resources -> JDBC -> JDBC Connection Pools
<br/>---------------------------------------
<br/>select exam pool
<br/>---------------------------------------
<br/>press Ping
