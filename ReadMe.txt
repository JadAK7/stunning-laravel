sudo: it is a command that gives a user administrative privilages to execute commands or run programs that require elevated permissions.
apt-get: it is a command that allows users ot install and manage software packages.
IP address: 52.48.246.65

To create .env, I used:
cp .env.example .env

sudo chgrp -R www-data storage bootstrap/cache
//chgrp changes the group name a file or directory belongs to. -R means recursively on all files in storage and bootstrap/cache. www-data is the group that they will be set to.

sudo chmod -R ug+rwx storage bootstrap/cache
//chmod means to change the file permissions. -R is to do it recursively, meaning on all files in storage and in boostrap/cache. ug+rwx means we're adding permissions to the owner and group, which are write, read, and execute.

https://computingforgeeks.com/install-php-mcrypt-extension-on-ubuntu/ to install php-mcrypt

Commands:
sudo apt-get update
sudo apt-get install apache2 mysql-server php-mysql php libapache2-mod-php php-pear curl php-curl php-cli git
sudo a2enmod rewrite
sudo service apache2 restart
cd /var/www/html
pwd
sudo git clone https://github.com/JadAK7/stunning-laravel.git
curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer
cd stunning-laravel
sudo composer install
pwd
cp .env.example .env
nano .env
sudo php artisan key:generate
which apache2
cd /usr/sbin
ls
nano apache2.conf
cd /etc/apache2/sites-enabled
nano 000-default.conf
sudo service apache2 restart
cd /var/www/html/stunning-laravel
sudo chgrp -R www-data storage bootstrap/cache
sudo chmod -R ug+rwx storage bootstrap/cache
