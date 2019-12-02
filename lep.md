# LEP setup for Laravel Project
```sh
$ sudo yum update -y
$ sudo amazon-linux-extras install nginx1
$ sudo service nginx start
$ ss -tlpn | grep :80
$ sudo amazon-linux-extras install php7.1/php7.2/php7.3
$ sudo yum install php-gd
$ sudo yum install php-dom
$ sudo yum install php-mbstring
$ sudo service php-fpm start
$ sudo vi /etc/php-fpm.d/www.conf
$ php-fpm ( initialize )
```

Composer Install 
curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
- composer install

# SSL setup
```sh
$ sudo amazon-linux-extras install epel
$ sudo yum install certbot-nginx
$ sudo iptables -I INPUT -p tcp -m tcp --dport 80 -j ACCEPT
$ sudo iptables -I INPUT -p tcp -m tcp --dport 443 -j ACCEPT
$ sudo certbot --nginx -d example.com -d www.example.com
$ sudo openssl dhparam -out /etc/ssl/certs/dhparam.pem 2048
# Auto renew
$ sudo certbot renew
$ sudo crontab -e
$ 15 3 * * * /usr/bin/certbot renew --quiet
```