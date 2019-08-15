
***********************************

## Install script for yiimp on Ubuntu 18.10

USE THIS SCRIPT ON FRESH INSTALL UBUNTU 18.10 !

Connect on your VPS =>
- adduser pool
- adduser pool sudo
- su - pool
- sudo apt-get -y install git
- git clone https://github.com/proteanx/yiimp_install_scrypt_ubuntu18.04.git
- cd yiimp_install_scrypt_ubuntu18.04/
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

**This install script will get you 95% ready to go with yiimp. There are a few things you need to do after the main install is finished.**

While I did add some server security to the script, it is every server owners responsibility to fully secure their own servers. After the installation you will still need to customize your serverconfig.php file to your liking, add your API keys, and build/add your coins to the control panel. 

There will be several wallets already in yiimp. These have nothing to do with the installation script and are from the database import from the yiimp github. 

