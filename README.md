# Project-Linux-Server-Configuration
This is the final project under Udacity Full Stack Nanodegree course. The project composes of deploying a Flask application onto a Linux server with all the essential softwares installed.

## Project Overview
You will take a baseline installation of a Linux server and prepare it to host your web applications. You will secure your server from a number of attack vectors, install and configure a database server, and deploy one of your existing web applications onto it.

## Why this Project?
A deep understanding of exactly what your web applications are doing, how they are hosted, and the interactions between multiple systems are what define you as a Full Stack Web Developer. In this project, you’ll be responsible for turning a brand-new, bare bones, Linux server into the secure and efficient web application host your applications need.

## What will I Learn?
You will learn how to access, secure, and perform the initial configuration of a bare-bones Linux server. You will then learn how to install and configure a web and database server and actually host a web application

## Get started on Ligtsail
We're recommending Amazon Lightsail for this project. If you prefer, you can use any other service that gives you a publicly accessible Ubuntu Linux server. But Lightsail works pretty well and it's what we've tested.

There are a few things you need to do when you create your server instance.

1. Log in
First, log in to Lightsail. If you don't already have an Amazon Web Services account, you'll be prompted to create one. Amazon Web Services login page.

![](https://camo.githubusercontent.com/b04c6f013ef9c3426fae8b913c556ed196cb0d58/68747470733a2f2f64313768323774366835313561352e636c6f756466726f6e742e6e65742f746f706865722f323031372f46656272756172792f35383965343566395f73637265656e2d73686f742d323031372d30322d31302d61742d31342e35392e33352f73637265656e2d73686f742d323031372d30322d31302d61742d31342e35392e33352e706e67)

Amazon Web Services login page.

2. Create an instance
Once you're logged in, Lightsail will give you a friendly message with a robot on it, prompting you to create an instance. A Lightsail instance is a Linux server running on a virtual machine inside an Amazon datacenter. When you have no instances, Lightsail gives you a picture of an orange robot and suggests that you create an instance.

![](https://camo.githubusercontent.com/889eb93426113892bd71cd2a7df6a6b093e9c030/68747470733a2f2f64313768323774366835313561352e636c6f756466726f6e742e6e65742f746f706865722f323031372f46656272756172792f35383965343561305f73637265656e2d73686f742d323031372d30322d31302d61742d31342e35382e31372f73637265656e2d73686f742d323031372d30322d31302d61742d31342e35382e31372e706e67)

When you have no instances, Lightsail gives you a picture of an orange robot and suggests that you create an instance.

3. Choose an instance image: Ubuntu
Lightsail supports a lot of different instance types. An instance image is a particular software setup, including an operating system and optionally built-in applications.

For this project, you'll want a plain Ubuntu Linux image. There are two settings to make here. First, choose "OS Only" (rather than "Apps + OS"). Second, choose Ubuntu as the operating system. When you create an instance, Lightsail asks what kind you want.For this project, choose an "OS Only" instance with Ubuntu.

![](https://camo.githubusercontent.com/89e35431a70e578602b33830af5629f99a48e877/68747470733a2f2f64313768323774366835313561352e636c6f756466726f6e742e6e65742f746f706865722f323031372f46656272756172792f35383965343363365f73637265656e2d73686f742d323031372d30322d31302d61742d31342e34362e31352f73637265656e2d73686f742d323031372d30322d31302d61742d31342e34362e31352e706e67)

When you create an instance, Lightsail asks what kind you want. For this project, choose an "OS Only" instance with Ubuntu.

4. Choose your instance plan
The instance plan controls how powerful of a server you get. It also controls how much money they want to charge you. For this project, the lowest tier of instance is just fine. And as long as you complete the project within a month and shut your instance down, the price will be zero. Lightsail's options for instance pricing.For this project, pick the lowest one to get free-tier access. Lightsail's options for instance pricing. For this project, pick the lowest one to get free-tier access.

![](https://camo.githubusercontent.com/1faac55eeff666e83e14ab80109efb7804204041/68747470733a2f2f64313768323774366835313561352e636c6f756466726f6e742e6e65742f746f706865722f323031372f46656272756172792f35383965343363615f73637265656e2d73686f742d323031372d30322d31302d61742d31342e34362e33352f73637265656e2d73686f742d323031372d30322d31302d61742d31342e34362e33352e706e67)

5. Give your instance a hostname
Every instance needs a unique hostname. You can use any name you like, as long as it doesn't have spaces or unusual characters in it. Your instance's name will be visible to you and to the project reviewer.

![](https://camo.githubusercontent.com/7e46932122ccfbddcf03a015bdf0c715d0728935/68747470733a2f2f64313768323774366835313561352e636c6f756466726f6e742e6e65742f746f706865722f323031372f46656272756172792f35383965343363655f73637265656e2d73686f742d323031372d30322d31302d61742d31342e34372e30382f73637265656e2d73686f742d323031372d30322d31302d61742d31342e34372e30382e706e67)

I've named my instance Udacity_Full_Stack.

6. Wait for it to start up.
It may take a few minutes for your instance to start up. While your instance is starting up, Lightsail shows you a grayed-out display.

While your instance is starting up, Lightsail shows you a grayed-out display.
Once your instance is running, the display gets brighter.

7. It's running; let's use it!
Once your instance has started up, you can log into it with SSH from your browser.

The public IP address of the instance is displayed along with its name. The big orange "Connect using SSH" button is the next step.

Explore the other tabs of this user interface to find the Lightsail firewall and other settings. You'll need to configure the Lightsail firewall as one step of the project.

When you SSH in, you'll be logged as the ubuntu user. When you want to execute commands as root, you'll need to use the sudo command to do it. Review sudo here if you need a refresher!

An SSH window logged into the server instance. From here, it's just like any other Linux server. An SSH window logged into the server instance. From here, it's just like any other Linux server.

8. Project time.
Now that you have a working instance, you can get right into the project.

## SSH into your server

* My IP address: `35.154.229.94`
* SSH port: `2200`
* Download private key from the SSH keys section in the Account section on Amazon Lightsail. The file name should be like `LightsailDefaultPrivateKey-us-east-2.pem`
* Create a new file named `lightsail_key.rsa` under ~/.ssh folder on your local machine
* Copy and paste content from downloaded private key file to `lightsail_key.rsa`
* Set file permission as owner only : `$ chmod 600 ~/.ssh/lightsail_key.rsa`
* SSH into the instance: `$ ssh -i ~/.ssh/lightsail_key.rsa ubuntu@35.154.229.94`

## Update the packages

* Run `sudo apt-get update` to update packages
* Run `sudo apt-get upgrade` to install newest versions of packages
* Set for future updates: `sudo apt-get dist-upgrade`

## Configuring the timezone to UTC

* `sudo dpkg-reconfigure tzdata`
* Select `None of the above`
* Select `UTC`

## Update SSH port from 22 to 200

* Run `$ sudo nano /etc/ssh/sshd_config` to open up the configuration file
* Change the port number from `22` to `2200` in this file
* Save and exit the file
* Restart SSH: `$ sudo service ssh restart`

## Configuring the firewall

* Check firewall status: `$ sudo ufw status`
* Set default firewall to deny all incomings: `$ sudo ufw default deny incoming`
* Set default firewall to allow all outgoings: `$ sudo ufw default allow outgoing`
* Allow incoming TCP packets on port 2200 to allow SSH: `$ sudo ufw allow 2200/tcp`
* Allow incoming TCP packets on port 80 to allow www: `$ sudo ufw allow www`
* Allow incoming UDP packets on port 123 to allow NTP: `$ sudo ufw allow 123/udp`
* Close port 22: `$ sudo ufw deny 22`
* Enable firewall: `$ sudo ufw enable`
* Check out current firewall status: `$ sudo ufw status`
* It should look as shown below
```
To                         Action      From`
--                         ------      ----`
22                         DENY        Anywhere
2200/tcp                   ALLOW       Anywhere
80/tcp                     ALLOW       Anywhere
123/udp                    ALLOW       Anywhere
22 (v6)                    DENY        Anywhere (v6)
2200/tcp (v6)              ALLOW       Anywhere (v6)
80/tcp (v6)                ALLOW       Anywhere (v6)
123/udp (v6)               ALLOW       Anywhere (v6)
```

* Update the firewall configuration on Amazon Lightsail website under Networking. Delete default SSH port `22 and add port 80, 123, 2200`
* Open up a new terminal and you can now ssh in via the new port 2200: `$ ssh -i ~/.ssh/lightsail_key.rsa ubuntu@35.154.229.94 -p 2200`

## Add new user grader

* Add a new user grader: `$ sudo adduser grader`
* `$ sudo nano /etc/sudoers`
* Create a file named `grader` under this path: `$ sudo touch /etc/sudoers.d/grader`
* `$ sudo nano /etc/sudoers.d/grader` 
* Add the line `grader ALL=(ALL:ALL) ALL` 
* Save and exit.

## Create SSH login for grader using keys

* Create a key-pair for grader using `ssh-keygen` on local machine
* Save it in `~/.ssh` path
* Now create or deploy the key in SSH environment.
  1. On local machine, read the public key that was generated using `cat ~/.ssh/FILE_NAME.pub`
  2. On virtual environment 
  ```
  $ mkdir .ssh
  $ touch .ssh/authorized_keys
  $ nano .ssh/authorized_keys
  $ sudo chmod 700 /home/grader/.ssh
  $ sudo chmod 644 /home/grader/.ssh/authorized_keys
  $ sudo chown -R grader:grader /home/grader/.ssh
  $ sudo service ssh restart
  ```
* Copy the generated public key from local machine and write it into **authorized_keys**  
* Now login as grader in port 2200: `$ ssh -i ~/.ssh/lightsail_key.rsa grader@35.154.229.94 -p 2200`
* To disable root login and to disable password for grader do the following `$ sudo nano /etc/ssh/sshd_config`
* Change `PermitRootLogin without-password` to `PermitRootLogin no` and change `PasswordAuthentication yes` to `PasswordAuthentication no`
* Restart SSH: `$ sudo service ssh restart`

## Installing Apache

* Install Apache by running the command: `$ sudo apt-get install apache2`
* Go to your IP Address and check if Apache is running. Apache home page will be shown. (http://35.154.229.94/)

## Installing PostgreSQL

* Run `$ sudo apt-get install postgresql`
* Open file: `$ sudo nano /etc/postgresql/9.5/main/pg_hba.conf`
* Check and make sure it looks as shown as below
```
# Database administrative login by Unix domain socket
local   all             postgres                                peer

# TYPE  DATABASE        USER            ADDRESS                 METHOD

# "local" is for Unix domain socket connections only
local   all             all                                     peer
# IPv4 local connections:
host    all             all             127.0.0.1/32            md5
# IPv6 local connections:
host    all             all             ::1/128                 md5
```

## Installing Python mod_wsgi

* Install the **mod_wsgi package**:  `$ sudo apt-get install libapache2-mod-wsgi-py3`
* Enable mod_wsgi: `$ sudo a2enmod wsgi`
* Restart Apache: `$ sudo service apache2 restart`
* Check if Python is installed: `$ python`
* Check python version: `$ python --version`

## Create database and new user catalog

* Switch to default **postgres** user from **grader**: `sudo su - postgres`
* Connect to PSQL: `$ psql`
```
postgres=# create database catalog;
postgres=# create user catalog;
postgres=# create role catalog with password '####';
postgres=# alter role catalog login;
postgres=# grant all privileges on database catalog to catalog;
```
* Connect to catalog DB: `\c catalog`
* Exit psql: `\q`
* Exit **postgres**: `exit`

## Installing Git

* `sudo apt-get install git`

## Cloning Item-catalog application from Github

* Create directory: `$ mkdir /var/www/app`
* Change to the directory: `$ cd /var/www/app`
* Clone the item-catalog app: `$ sudo git clone https://github.com/Varadhu93/Item-catalog-application.git app`
* Change the ownership: `$ sudo chown -R grader:grader app/`
* Install the required libraries and dependencies: `sudo pip install -r requirements.txt`

## Mandatory libraries to make your application run

* Install pip based on python version: `$ sudo apt-get install python-pip` or `$ sudo apt-get install python-pip3`
* Install libraries: 
```
$ sudo pip install httplib2 or sudo pip3 install httplib2 
$ sudo pip install requests or sudo pip3 install requests
$ sudo pip install --upgrade oauth2client or sudo pip3 install --upgrade oauth2client
$ sudo pip install sqlalchemy or sudo pip3 install sqlalchemy
$ sudo pip install flask or sudo pip3 install flask
$ sudo apt-get install libpq-dev or sudo apt-get install libpq-dev 
```
* Changing from SQLite to PostgreSQL will require installation of psycopg2 after Python is installed.
`$ sudo pip install psycopg2 or sudo pip3 install psycopg2`
## Configuring virtual host

* Create a file using command: `$ sudo nano /etc/apache2/sites-available/app.conf`
```
<VirtualHost *:80>
  ServerName 35.154.229.94 
  ServerAdmin varadhu93amrita@gmail.com
  WSGIScriptAlias / /var/www/app/app.wsgi
<Directory /var/www/app/app/>
  Order allow,deny
  Allow from all
</Directory>
  Alias /static /var/www/app/app/static
<Directory /var/www/app/app/static/>
  Order allow,deny
  Allow from all
</Directory>
  ErrorLog ${APACHE_LOG_DIR}/error.log
  LogLevel warn
  CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```
* Enable the virtualhost using command: `sudo a2ensite app`
* Restart or reload **Apache:** `$ sudo service apache2 reload`

## Configuring .wsgi file

* Create a file: `$ sudo touch /var/www/app/app.wsgi`
* Add the following content
```
#!/usr/bin/python3
import socket
from socket import socket
import sys
import logging
logging.basicConfig(stream=sys.stderr)
sys.path.insert(0, "/var/www/app/app/")
sys.path.insert(1, "/var/www/app/")

from application import app as application
application.secret_key = 'super_secret_key'
```
* Restart **Apache**: `$ sudo service apache2 reload`

## Configuring database path and client_secrets.json path
* Modify the line in `application.py, database_setup.py, database_data.py` as shown below
`engine = create_engine('postgresql://catalog:INSERT_PASSWORD_FOR_DATABASE_HERE@localhost/catalog')`
* Change paths to the client_secrets.json file, and any other external files, to absolute. 
```
$ cd /var/www/app
$ sudo nano application.py
```
`CLIENT_SECRET = json.loads(open('/var/www/app/app/client_secrets.json', 'r')
                          .read())['web']['client_secret']`

## Disable default Apache

* `$ sudo a2dissite 000-defualt.conf`
* Restart **Apache**: `$ sudo service apache2 reload`

## Setting up the database

* Run `$ sudo python3 application.py`
* Run `$ sudo python3 database_setup.py`
* Run `$ sudo python3 database_data.py`
* Restart **Apache**: `$ sudo service apache2 reload`
* Now follow the link to http://35.154.229.94/ the application should be running online

## Troubleshooting

* If internal errors occur: check the Apache error file logs
``` 
$ sudo tail /var/log/apache2/error.log
$ sudo tail /var/log/apache2/access.log
```
## References

* [Udacity Full Stack Course](https://classroom.udacity.com)
* [DigitalOcean](digitalocean.com)
* [askubuntu](https://askubuntu.com)
* [Stackoverflow](https://stackoverflow.com)
* [PostgreSQL](www.postgresql.org)
