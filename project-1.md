## PROJECT 1: LAMP STACK IMPLEMENTATION

### I started the Installation of Apache using Ubuntu’s package manager

### First, I started by updating the list of packages in package manager by running the below command.

 `sudo apt update`

 ![apt update](./images/apt-update.jpg)

 ### Run apache2 package installation by running the command "sudo apt install apache2"

 `sudo apt install apache2`

 ![apache2 installation](./images/apache2-installation.jpg)

 ### Run apache2 package installation by running the command "sudo apt install apache2"

 `sudo apt install apache2`

 ![apache2 installation](./images/apache2-status.jpg)

### To receive any traffic in our Web Server, we need to open TCP port 80 which is the default port that web browsers use to access web pages on the Internet.
### - Check the box in front of the EC2 instance, select security, and click on security group link, and click on edit inbound rule, add HTTP configuration inbound connection through protocol with default port 80 as shown below.

 ![HTTP port80](./images/HTTP-port-80.jpg)

 ### To check if we can access it locally in our Ubuntu shell, we have to run the below command.

 `curl http://localhost:80`, or `curl http://127.0.0.1:8`

![local host access](./images/localhost-access.jpg)

![local host access1](./images/local-host-access1.jpg)

### To test and confirm how our Apache HTTP server responds to requests from the Internet. I opened the Microsoft Edge web browser and ran the below http link through my url, and the web server is correctly installed and accessible through my firewall.

`http://3.84.6.47:80`

### - I also use the below command to retrive my AWS Web console public IP

`curl -s http://169.254.169.254/latest/meta-data/public-ipv4`

![Apache HTTP server responds](./images/Apache-HTTP-server-responds.jpg)

## STEP 2 — INSTALLING MYSQL

### To help store and manage data for my Apache web Server, MYSQL database management system (DBMS) will be installed using the below command, and then confirm yes (y) for additional disk space of 242 M to be used.

`sudo apt install mysql-server`

![Mysql installation](./images/Mysql-installation.jpg)

![Mysql installation](./images/Mysql-installation1.jpg)

### Starting the interactive script for the security script that comes pre-install with MySQL to remove some insecure default settings and lock down access to the database system

### Before running the script I will set a password for the root user, by using mysql_native_password as default authentication method, and define the user’s password as PassWord.1.

### Firstly, we run the below command and exit MySQL.

`ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';`

![Alter User](./images/ALTER-USER.jpg)

#### secondly, I will Start the interactive script by running the below command, and to respond to other questions, enter Y and hit the ENTER key at each prompt to change the root password, remove some anonymous users and the test database, disable remote root logins, and load these new rules so that MySQL immediately respects the changes I have made.

`sudo mysql_secure_installation`

![Mysql Secure](./images/mysql-secure.jpg)

![Mysql Secure](./images/mysql-secure1.jpg)

#### To test if I am able to login to MySQL console, I run the below command, and exit MySQL console.

`sudo mysql -p`

![Mysql Login](./images/confirm-lmysql-ogin.jpg)

## STEP 3 — INSTALLING PHP

#### To install PHP and the additional component of the php package, I will have to install php-mysql, PHP module that allows PHP to communicate with MySQL-based databases, and libapache2-mod-php is needed to enable Apache to handle PHP files.

### The below command will be ran to Install the three (3) PHP pakages at the same time.

`sudo apt install php libapache2-mod-php php-mysql`

![PHP and 3 pakage Installation](./images/PHP-3-Installation.jpg)

![PHP and 3 pakage Installation](./images/PHP-3-Installation1.jpg)

## Confirm PHP version running

#### To confirm the PHP version running on the server, the below command is use.

`php v`

![confirm PHP version](./images/PHP%20Version.jpg)

### I have install LAMP stack, and it is full operational.

### Use the link below to preview project-1 implementation.
- [PROJECT 1: LAMP STACK IMPLEMENTATION](https://github.com/Tasbaba/Project-1/blob/main/project-1.md)






 