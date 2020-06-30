### Script description

ILNMP (Installation Linux Nginx MySQL PHP) is a lightweight, extremely simplified, automated, unattended PHP integrated environment installation script that supports the installation of the latest technology stack version. The iLNMP script supports a high degree of customization, and the code is transparent, no bloated redundant code, no junk data output, and the corresponding software package is automatically deleted after the installation is successful, which occupies little disk space. Compared with the control panel, the expenditure on security, CPU, memory, network and other resources is greatly reduced.

The script is written in Shell and can deploy the latest version of Nginx/MariaDB/MySQL/PHP/phpMyadmin to the production environment. It is suitable for CentOS 7 ~ 8 and Redhat 7 ~ 8 64-bit operating systems.


### Script properties

- Support Nginx 1.x
- Support MariaDB 10.x
- Support MySQL 8.x
- Support PHP7.4.x
- Support phpMyAdmin 5.x
- Must be installed online
- Linux distributions below CentOS 7 are not supported
- 32-bit operating systems are not supported

### installation

```bash
bash ilnmp.sh
```

### Software installation path description

|iLNMP installation path|Remarks|
| ------------ | ------------ |
|/apps|All software installation directory|
|/apps/server/nginx|Nginx installation directory|
|/apps/server/mariadb|MariaDB installation directory|
|/apps/server/mariadb/data|MariaDB data storage directory|
|/apps/server/mysql|MySQL installation directory|
|/apps/server/mysql/data |MySQL data storage directory|
|/apps/server/php |PHP installation directory|
|/apps/server/php/etc|PHP configuration file directory|
|/apps/web/default|Website default directory|
|/apps/web/default/phpmyadmin |Database management tools directory|
|/apps/web/default/php.php|PHP Probe|

### How to manage service

Nginx：

```bash
systemctl {start|stop|status|restart} nginx.service

```
MariaDB/MySQL:

```bash
systemctl {start|stop|status|restart} mysqld

```
PHP:

```bash
systemctl {start|stop|status|restart} php-fpm.service

```
### How to uninstall

```bash
rm -rf /apps
rm -rf /etc/my.cnf
rm -rf /etc/init.d/mysqld
rm -rf /lib/systemd/system/nginx.service
rm -rf /lib/systemd/system/php-fpm.service
```
