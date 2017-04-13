# Add Jessie backports and PHP7 APT repo
wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg
gpg --keyserver pgpkeys.mit.edu --recv-key [Insert here your missing key ID]
gpg -a --export [Insert here your missing key ID] | sudo apt-key add -  

echo "deb http://ftp.debian.org/debian jessie-backports main" > /etc/apt/sources.list.d/debian-backports.list
echo "deb https://packages.sury.org/php/ jessie main" > /etc/apt/sources.list.d/php.list

# Installed packages
- apt-transport-https
- nginx -t jessie-backports
- openssl -t jessie-backports
- certbot -t jessie-backports
- ufw
- fail2ban
- htop
- php7.0-fpm
- php7.0-mysql

# Disable ROOT user
sudo passwd -l root

# Resources
Pi Watchdog: http://www.theengineeringhitman.com/setting-raspberry-pi-watchdog-timer/  
Pestmeester: https://www.pestmeester.nl/  
Mozilla secure SSL: https://mozilla.github.io/server-side-tls/ssl-config-generator/  
Pi Netinstall: https://github.com/FooDeas/raspberrypi-ua-netinst  
Cipherli.st: https://cipherli.st/  
Perfect Nginx sample: http://blog.commando.io/the-perfect-nginx-ssl-configuration/  
https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-debian-8  
https://snippets.khromov.se/change-dns-servers-for-a-debian-server/  
https://securityheaders.io  
https://www.linode.com/docs/websites/nginx/configure-nginx-for-optimized-performance  
