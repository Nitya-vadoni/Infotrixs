MONOLITH PROJECT-1

step-1: Create EC2 instance by selecting AMI ubuntu,t2 micro(free tier)

step-2: Login to virtual machine by using the ssh client.

step-3: Update the server's package list.
        sudo apt-get update

step-4: Install Apache server on Ubuntu
        sudo apt install apache2

step-5: Install php runtime and php mysql connector
        sudo apt install php libapache2-mod-php php-mysql

step-6: Install MySQL server
        sudo apt install mysql-server

step-7: Login to MySQL server
        sudo mysql -u root

step-8: Change authentication plugin to mysql_native_password (change the password to something strong)
        ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password by 'Testpassword@123';

step-9: Create a new database user for wordpress (change the password to something strong)[optional but recommended]
        CREATE USER 'wp_user'@localhost IDENTIFIED BY 'Testpassword@123';

step-10: Create a database for wordpress
         CREATE DATABASE wp;

step-11: show databases;

step-12: exit from the database(sql)

step-13: Download the wordpress from the url https://wordpress.org/latest.zip
	 wget https://wordpress.org/latest.zip

step-14: unzip the folder 
	 unzip latest.zip (after using this command if it shows the error install the unzip package by using the command sudo apt install unzip)

step-15: After unzip the folder check the files and folder.
	 ls

step-16: change the directory to wordpress
	 cd wordpress/

step-17: copy the content of wordpress folder to /var/www/html
	 cp -r * /var/www/html

step-18: check the permission of the html folder 
	 ll

step-19: change the permission of the html folder
	 sudo chmod -R 666 /var/www/html

step-20: remove the index.html file.
	 rm index.html

step-21: Copy the public ip of the Ec2 instance and paste in any of the browser hit enter it will ask the user id and password of database.

step-22: provide the user name and password click on submit button.

step-23: new window will get open give the new credentials such as  userid and password, click on install wordpress button.

step-24: click on Run the installation.

step-25: New login page will get open give the newly created user id and password click on Login   button.	 