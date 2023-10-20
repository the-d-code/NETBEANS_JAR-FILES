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

==========================================================================================
in Additional Properties section

Add this two Proerties
-------------------------------------
**driver** : com.mysql.jdbc.Driver
**driverClass** : com.mysql.jdbc.Driver

find this properties
-------------------------------------
**User** : PhpMyAdmin_Username
**Password** : PhpMyAdmin_Password
**ServerName** : localhost
**DatabaseName** : your_datbase_name
**URL** : jdbc:mysql://localhost:3306/your_datbase_name
URL : jdbc:mysql://localhost:3306/your_datbase_name
--------------------------------------
press Finish

# 3) for jndi

http://localhost:4848/common/index.jsf
---------------------------------------
from sidebar 
in Resources -> JDBC -> JDBC Resources -> New
---------------------------------------
JNDI Name : jdbc/exam // exam is pool name
Pool Name : exam
---------------------------------------
press OK

# 4) ping

http://localhost:4848/common/index.jsf
----------------------------------------
from sidebar 
in Resources -> JDBC -> JDBC Connection Pools
---------------------------------------
select exam pool
---------------------------------------
press Ping
