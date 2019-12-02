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