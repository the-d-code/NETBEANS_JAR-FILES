# 1) For All Property 

Payara_Server -> glassfish -> lib -> here place mysql-connector-java-5.0.8-bin.jar file

# 2) for pool connection

http://localhost:4848/common/index.jsf

from sidebar 
in Resources -> JDBC -> JDBC Connection Pools -> New

Pool Name : exam
Resource Type : javax.sql.DataSource
Database Driver Vendor : MySql

press Next

<br/>in Additional Properties section

Add this two Proerties

<br/>driver : com.mysql.jdbc.Driver<br/>
<br/>driverClass : com.mysql.jdbc.Driver

find this properties

<br/>User : PhpMyAdmin_Username
<br/>Password : PhpMyAdmin_Password
<br/>ServerName : localhost
<br/>DatabaseName : your_datbase_name
<br/>URL : jdbc:mysql://localhost:3306/your_datbase_name
<br/>URL : jdbc:mysql://localhost:3306/your_datbase_name

<br/>press Finish

# 3) for jndi

http://localhost:4848/common/index.jsf

from sidebar 

<br/>in Resources -> JDBC -> JDBC Resources -> New

<br/>JNDI Name : jdbc/exam // exam is pool name
<br/>Pool Name : exam

<br/>press OK

# 4) ping

http://localhost:4848/common/index.jsf
<br/>
<br/>from sidebar 
<br/>in Resources -> JDBC -> JDBC Connection Pools

<br/>select exam pool

<br/>press Ping





=======================================================<BR/>
ANACONDA 3 ENV SETUP COMMANDS                               
=======================================================<BR/>

NUMPY  = pip uninstall -y numpy
PANDAS = pip uninstall -y pandas
    
UNINSTALL = pip uninstall -y setuptools
INSTALL   = conda install setuptools

LIB = conda install numpy 
      conda install pandas
      conda install matlotlib

=======================================================<BR/>
SPYDER START USING CMD                              
=======================================================<BR/>
conda create -n spyder-env -c conda-forge spyder python=3.8
conda activate spyder-env
spyder
spyder --new-instance

=======================================================<BR/>
ORECL STOP COMMAND                              
=======================================================<BR/>
/etc/init.d/oracle-xe stop
