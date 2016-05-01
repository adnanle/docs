# Cài đặt Ubuntu 16.04 LTS 64bit

# Cài đặt Chrome và Sublime Text

```
sudo apt-get install gdebi
```

Tải và cài đặt Chrome, Sublime thông qua GDebi

# Cài đặt bộ gõ tiếng Việt cho Ubuntu

```
sudo apt-get install ibus-unikey
```

Logout & Login trở lại. Vào "Text Entry" để thêm "Vietnamese (Unikey) (IBus)" và "English US" vào.

# Cài bộ gõ tiếng Việt cho Sublime

- Cài đặt Package Control: https://packagecontrol.io/installation
- Cài đặt VN IME: https://packagecontrol.io/packages/Vn%20Ime

# Cài đặt Nginx

```
sudo apt-get install nginx
```

# Thêm website đầu tiên

Website này là website html, mục đích là dùng để chứa các template mua được. Điểm đáng lưu ý là có thể "browse" các thư mục.

```
cd ~
mkdir www
cd www
mkdir html
cp /var/www/html ~/www/html/nginx
sudo nano /etc/nginx/conf.d/template.conf
```

copy/paste nội dung file ```https://github.com/adnanle/docs/blob/master/snippets/Cai-Dat-Moi-Truong-Lam-Viec-nginx-template.conf``` vào

```
sudo nano /etc/hosts
```

thêm dòng sau vào file hosts

```
127.0.0.1       template.lc
```

# Install MariaDB, HHVM, Git, Composer 

```
sudo apt-get install mariadb-client mariadb-server
sudo apt-get install hhvm
sudo apt-get install git composer
sudo apt-get install libmcrypt-dev mcrypt
```

# Set root password to secure the MariaDB

```
sudo systemctl start mysql
sudo mysql_secure_installation
```

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
