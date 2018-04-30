# Install Pool


***********************************

## Install script for yiimp on Ubuntu 16.04

USE THIS SCRIPT ON FRESH INSTALL UBUNTU 16.04 !

Connect on your VPS =>
- adduser pool
- adduser pool sudo
- su - pool
- sudo apt-get -y install git
- git clone https://github.com/yalilia/pool.git
- cd yiimp_install_scrypt/
- sudo bash install.sh (Do not run the script as root)
- sudo bash screen-scrypt.sh (in tuto youtube, i launch the scrypt with root... it does not matter)
- NOT MANDATORY => sudo bash screen-stratum.sh (CONFIGURE BEFORE START this script... add or remove algo you use).

Finish !
Go http://xxx.xxxxxx.xxx or https://xxx.xxxxxx.xxx (if you have chosen LetsEncrypt SSL). Enjoy !

###### :bangbang: **YOU MUST UPDATE THE FOLLOWING FILES :**
- **/var/web/serverconfig.php :** update this file to include your public ip (line = YAAMP_ADMIN_IP) to access the admin panel (Put your PERSONNAL IP, NOT IP of your VPS). update with public keys from exchanges. update with other information specific to your server..
- **/etc/yiimp/keys.php :** update with secrect keys from the exchanges (not mandatory)


###### :bangbang: **IMPORTANT** : 

- The configuration of yiimp and coin require a minimum of knowledge in linux
- Your mysql information (login/Password) is saved in **~/.my.cnf**
- **If you reboot your VPS**, you must restart screen-scrypt.sh (or add crontab)
- Remember to restart **memcached service** after the db change (update or import new .sql)

***********************************

###### This script has an interactive beginning and will ask for the following information :

- Enter time zone
- Server Name 
- Are you using a subdomain
- Enter support email
- Set stratum to AutoExchange
- New location for /site/adminRights
- Your Public IP for admin access (Put your PERSONNAL IP, NOT IP of your VPS)
- Install Fail2ban
- Install UFW and configure ports
- Install LetsEncrypt SSL

***********************************


