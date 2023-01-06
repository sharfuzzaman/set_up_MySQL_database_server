
# How to install a MySQL database server in Linux

Install wget in your system first, We are going to download .deb package because debian linux has MariaDB database server instead of MySQL database server
```bash
   $ sudo apt-get install wget
```
After installed wget, now we can download our .deb package from https://dev.mysql.com
```bash
   $ wget https://dev.mysql.com/get/mysql-apt-config_0.8.13-1_all.deb
```
In my case i am downloading mysql-apt-config_0.8.13-1_all.deb package, You can download the latest package.
(mysql-apt-get-config_0.8.13-1_all.deb you’ll find this latest version on https://dev.mysql.com/downloads/repo/apt/ this url) 

If you do not have dpkg in your system please install it first,
```bash
   $ sudo apt install dpkg -y
```
Now we can install MySQL server.
```bash
   $ sudo dpkg -i *.deb
```
Here *deb (is referencing the package mysql-apt-config_0.8.13-1_all.deb  we have downloaded earlier)

```bash
   $ sudo apt update
   $ sudo apt install mysql-server
```
After, installed MySQL server check the version and server status
For check the version,
```bash
   $ mysql --version
```
You will have a output like this
<br><br>
![App Screenshot](https://github.com/sharfuzzaman/set_up_MySQL_database_server_linux/blob/main/mysql_version.png)
<br><br>
After that check the the MySQL server status,
```bash
   $ sudo service mysql status
```
After run this command it will look like this
<br><br>
![App Screenshot](https://github.com/sharfuzzaman/set_up_MySQL_database_server_linux/blob/main/mysql_status.png)
<br><br>
If you find the output like this, Hurray!! our MySQl database server is successfully installed.

#### For secure installation
We are left by few steps for secure installation, let's do it by now.
```bash
   $ sudo mysql_secure_installation
```
(It will ask for some queries, **please fill every query with caution. If you do not understand those queries read it again and again)**.

After completed the secure installation MySQL database server is ready to perform the task.
