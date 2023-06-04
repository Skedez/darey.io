## Web stack implementation (lamp stack) in aws

The first thing I did was to spin up an EC2 instance on AWS - Ubuntu - Free Tier
![image](https://github.com/Skedez/darey.io/assets/54313899/e24f19be-c2fe-4bc6-9cc6-d0a038af0f9e)

After doing this, I logged in via SSH using the GIT BASH application installed on my PC, There are other applications you can use for this as well. Example Termius which I also like. While creating the EC2 instance, I added an inbound rule accepting connections from HTTP and HTTPS ports so I could connect to the server via my Internet Browser

![image](https://github.com/Skedez/darey.io/assets/54313899/34a54cc7-6538-4720-a705-09234914c0a1)

I ran my sudo apt update to update all that needed to be updated (History of commands ran at the end of the presentation)
I installed APACHE2
I installed MYSQL-SERVER
I installed PHP

I created an index.html in my projectlamp directory which was also created.
I configured index.php file to be the first executable file in my dir.conf using sudo vim /etc/apache2/mods-enabled/dir.conf command
I created an index.php file and configured phpinfo to display on this file. I verified this with my public IP address on my browser.
I then created an index.html file in my projectlamp directory. I deleted the index.php file making the index.html file be the first on the prioroty list.

![image](https://github.com/Skedez/darey.io/assets/54313899/e83562af-83a2-42af-93c8-ef869eade1c4)

Below is a list of all commands ran in the execution of this project.

ubuntu@ip-172-31-84-8:/$ history
    1  ls
    2  pwd
    3  clear
    4  exit
    5  sudo apt update
    6  sudo apt install apache2
    7  which apache2
    8  sudo which apache2
    9  sudo systemctl status apache2
   10  curl 127.0.0.1:80
   11  curl -s http://169.254.169.254/latest/meta-data/public-ipv4
   12  sudo apt install mysql-server
   13  which mysql
   14  which apache
   15  which apache2
   16  mysql
   17  sudo mysql
   18  ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';
   19  sudo mysql
   20  sudo mysql_secure_installation
   21  sudo mysql
   22  sudo mysql-server
   23  sudo mysql
   24  sudo mysql -p
   25  sudo apt install php libapache2-mod-php php-mysql
   26  which php
   27  which apache2
   28  which mysql'
which mysql

exit

   29  which mysql-server
   30  sudo mysql -p
   31  php -v
   32  mysql -p
   33  sudo mysql -p
   34  clear
   35  ls
   36  cd ..
   37  pwd
   38  cd
   39  cd /var/
   40  cd www/
   41  cd html/
   42  ls
   43  mkdir projectlamp
   44  sudo mkdir projectlamp
   45  ls
   46  cd ..
   47  cd /var/www/
   48  ls
   49  cd html/
   50  ls
   51  rmdir projectlamp/
   52  sudp rmdir projectlamp/
   53  sudo rmdir projectlamp/
   54  ls
   55  ll
   56  ls
   57  cd ..
   58  sudo mkdir /var/www/projectlamp
   59  sudo vi /etc/apache2/sites-available/projectlamp.conf
   60  sudo ls /etc/apache2/sites-available/
   61  sudo a2ensite projectlamp.conf
   62  sudo systemctl reload apache2
   63  sudo a2dissite 000-default.conf
   64  sudo systemctl reload apache2
   65  sudo apache2ctl configtest
   66  sudo systemctl reload apache2
   67  sudo echo 'Hello LAMP from hostname' $(curl -s http://169.254.169.254/latest/meta-data/public-hostname) 'with public IP' $(curl -s http://169.254.169.254/latest/meta-data/public-ipv4) > /var/www/projectlamp/index.html
   68  ls /var/www/
   69  ls /var/www/projectlamp/
   70  vi /var/www/projectlamp/index.html
   71  sudo vim /etc/apache2/mods-enabled/dir.conf
   72  sudo systemctl reload apache2
   73  vi /var/www/projectlamp/index.php
   74  ls /var/www/projectlamp/
   75  php -v
   76  sudo rm /var/www/projectlamp/index.php
   77  vi /var/www/projectlamp/index.html
   78  rm /var/www/projectlamp/index.html
   79  vi /var/www/projectlamp/index.html
   80  clear
   81  history
ubuntu@ip-172-31-84-8:/$ ^C

## Thank you









