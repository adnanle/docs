# Initial Server

- https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-16-04

# Install Nginx

- https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-16-04

# Install HHVM, Composer 

```
sudo apt-get install hhvm
sudo apt-get install composer
```

# Install MariaDB

- https://downloads.mariadb.org/mariadb/repositories

# Install PHP extensions:

```
sudo apt-get install php-mbstring
sudo apt-get install php-dom
```

# HHVM Configuration

## server.ini
```
sudo nano /etc/hhvm/server.ini
```

and add this lines

```
; support PHP7
hhvm.php7.all = 1
```

## User to run hhvm
```
sudo nano /etc/default/hhvm
```

and change edit this to your user and group

```
RUN_AS_USER="www-data"
RUN_AS_GROUP="www-data"
```
