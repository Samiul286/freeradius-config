# freeradius-config
PHPNuxBill Installation Shell Script, this script will guide you through the installation and configuration of the following components:
- LAMP stack (Linux, Apache, MySQL/MariaDB, PHP 8.2+)
* FreeRADIUS for authentication and authorization
+ PHPNuxBill for billing and network management

## Install using GIT
```
sudo apt-get install git
```
```
sudo git clone https://github.com/Samiul286/freeradius-config.git
```
```
cd freeradius-config
sudo chmod +x install.sh
sudo ./install.sh
```
## Install using WGET
```
sudo apt-get install wget unzip
```
```
wget https://github.com/Samiul286/freeradius-config/archive/refs/heads/main.zip
unzip *.zip
```
```
sudo mv freeradius-config-main freeradius-config
cd freeradius-config
sudo chmod +x install.sh
sudo ./install.sh
```

## Note
After Successful Installation without error
Visit http://host-or-ip/phpnuxbill/ 
Replace [host-or-ip] with your ip address or hostname
You may wish to move the files to root folder, so that you can access nuxbill directly without sub-folder e.g http://host-or-ip/ and also remove index.html the default apache file
```
sudo mv /var/www/html/phpnuxbill/* /var/www/html
sudo chown -R www-data:www-data /var/www/html
sudo chmod -R 755 /var/www/html
cd /var/www/html/
sudo rm -i index.html
cd

```

## Tested
This shell script is tested successfully on

- **Ubuntu 24.04  LTS**
- **Ubuntu 22.04  LTS**
- **Ubuntu 20.04  LTS**
- **Ubuntu 18.04  LTS**
- **Debian 10, 11, 12**

## PHP Version
This script installs **PHP 8.2** (or higher) using the `ondrej/php` PPA, ensuring compatibility with the latest PHPNuxBill requirements.
