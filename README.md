This is a modified version of MorbZ/munin-php-fpm https://github.com/MorbZ/munin-php-fpm

Setup PHP-FPM
-------------

This plugin requires PHP CLI.

### Install Plugin
`$ cd /usr/share/munin/plugins/`  
`$ [sudo] wget -O php-fpm https://raw.github.com/danpospisil/munin-php-fpm/master/php-fpm.php`  
`$ [sudo] chmod +x php-fpm`

### Setup Graphs
Average process memory per pool:  
`$ [sudo] ln -s /usr/share/munin/plugins/php-fpm /etc/munin/plugins/php-fpm-memory`

CPU per pool:  
`$ [sudo] ln -s /usr/share/munin/plugins/php-fpm /etc/munin/plugins/php-fpm-cpu`

Number of processes per pool:  
`$ [sudo] ln -s /usr/share/munin/plugins/php-fpm /etc/munin/plugins/php-fpm-count`

Average process age per pool:  
`$ [sudo] ln -s /usr/share/munin/plugins/php-fpm /etc/munin/plugins/php-fpm-time`

Don't forget to restart Munin after changing plugins:  
`$ [sudo] service munin-node restart`