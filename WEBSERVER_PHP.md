      Install Apache
        sudo yum install httpd mod_sll
        sudo /usr/sbin/apachectl start

      Configure Sites  
        sudo nano /etc/httpd/conf/httpd.conf
          #ServerName www.example.com:80
          ServerName demo

        sudo /usr/sbin/apachectl restart

      Open Ports
        sudo iptables -I INPUT -p tcp --dport 80 -j ACCEPT
        sudo service iptables save

      Testing
        sudo /sbin/chkconfig httpd on
        sudo /sbin/chkconfig --list httpd

      PHP
        sudo yum install php php-mysql php-devel php-gd php-pecl-memcache php-pspell php-snmp php-xmlrpc php-xml
        sudo /usr/sbin/apachectl restart
