# LEN setup for Javascript Project
```sh
$ sudo yum update -y
$ sudo yum install node
$ ps aux | grep node
$ sudo npm install pm2@latest -g
$ pm2 start npm --name "myapp" -- run scripts:name
```