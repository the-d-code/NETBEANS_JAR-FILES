# PAYARA PING CONNECTION SETUP WITH PING CONNECTION

**=======================================================<BR/>
1 CHECK JAR FILE IS THERE OR NOT ?<BR/>                            
=======================================================<BR/>**

Payara_Server -> glassfish -> lib -> here place all jar file in this repo <br/>
Payara_Server -> glassfish -> domain -> domain1 -> lib -> here place all jar file in this repo 

**=======================================================<BR/>
2) Creation Of Pull Connection<BR/>                            
=======================================================<BR/>**
http://localhost:4848/common/index.jsf

**from sidebar** 
in Resources -> JDBC -> JDBC Connection Pools -> New

Pool Name : exam
Resource Type : javax.sql.DataSource
Database Driver Vendor : MySql

press Next

**<br/>in Additional Properties section**

Add this two Proerties

<br/>driver : com.mysql.jdbc.Driver<br/>
<br/>driverClass : com.mysql.jdbc.Driver

**find this properties**

<br/>User : PhpMyAdmin_Username
<br/>Password : PhpMyAdmin_Password
<br/>ServerName : localhost
<br/>DatabaseName : your_datbase_name
<br/>URL : jdbc:mysql://localhost:3306/your_datbase_name
<br/>URL : jdbc:mysql://localhost:3306/your_datbase_name

<br/>press Finish

**=======================================================<BR/>
3) Creating JNDI Connection<BR/>                             
=======================================================<BR/>**
http://localhost:4848/common/index.jsf

**from sidebar **

<br/>in Resources -> JDBC -> JDBC Resources -> New

<br/>JNDI Name : jdbc/exam // exam is pool name
<br/>Pool Name : exam

<br/>press OK

**=======================================================<BR/>
4) Ping Connection<BR/>
=======================================================<BR/>**
http://localhost:4848/common/index.jsf

<br/>
**<br/>from sidebar **

<br/>in Resources -> JDBC -> JDBC Connection Pools

<br/>select exam pool

<br/>press Ping



# Anaconda

**=======================================================<BR/>
ANACONDA 3 ENV SETUP COMMANDS                               
=======================================================<BR/>**

NUMPY  = pip uninstall -y numpy<br/>
PANDAS = pip uninstall -y pandas
    
UNINSTALL = pip uninstall -y setuptools<br/>
INSTALL   = conda install setuptools

LIB = conda install numpy <br/>
      conda install pandas<br/>
      conda install matlotlib

**=======================================================<BR/>
SPYDER START USING CMD                              
=======================================================<BR/>**
conda create -n spyder-env -c conda-forge spyder python=3.8<BR/>
conda activate spyder-env<BR/>
spyder<BR/>
spyder --new-instance

**=======================================================<BR/>
ORECL STOP COMMAND                              
=======================================================<BR/>**
/etc/init.d/oracle-xe stop
