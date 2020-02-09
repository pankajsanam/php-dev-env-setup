# Development Setup
Setup a dev environment on Ubuntu for PHP and node.

## Setup Dev Environment

Run the updates-

```
sudo apt update

sudo apt upgrade
```

Install and start apache2-
```
sudo apt install apache2

sudo systemctl enable apache2

sudo systemctl start apache2
```

Install and setup database-
```
sudo apt install mysql-server

mysql_secure_installation
```

Install PHP 7.3-
```
sudo apt install php7.3 \
  php7.3-bcmath \
  php7.3-cli \
  php7.3-common \
  php7.3-curl \
  php7.3-gd \
  php7.3-intl \
  php7.3-json \
  php7.3-mbstring \
  php7.3-mysql \
  php7.3-opcache \
  php7.3-xml \
  php7.3-soap \
  php7.3-zip
```

Test the PHP-
```
cd /var/www/html

sudo nano info.php 
```

Write this in info.php and run it to check if everything is working fine-
```php
<?php

phpinfo();

?>
```

Install phpmyadmin to access database-
```
sudo apt install phpmyadmin
```

Increase max_execution_time, max_input_time, memory_limit, post_max_size in php.ini-
```
sudo nano /etc/php/7.3/apache2/php.ini
```

Update default configuration for apache-
```
sudo nano /etc/apache2/sites-available/000-default.conf
```

Enable rewrite module in apache-
```
sudo a2enmod rewrite

sudo systemctl restart apache2
```

#### Note:
In case you have two php versions installed you can remove one by this command-

```
sudo apt purge php7.2*
```

Install Git- 

```
sudo apt install git
```

Install Node through nvm-
Follow this to intall node version manager-
https://github.com/nvm-sh/nvm

Install Composer-
```
curl -s https://getcomposer.org/installer | php

sudo mv composer.phar /usr/local/bin/composer

composer
```
