# upgrade manjaro php bug and terminal bug

Solved bug upgrade manjaro localhost and terminal - February 2021


####### localhost #######
# In file:
gedit /etc/httpd/conf

# change line aprox 184
LoadModule php7_module modules/libphp7.so
# to
LoadModule php_module modules/libphp.so

# and end file
Include conf/extra/php7_module.conf
# to
Include conf/extra/php_module.conf

# restart apache
sudo systemctl restart httpd
sudo systemctl status httpd


####### terminal #######

# Install vscode and run (open terminar ctrl+shift+´)
# Software Install

# uncomment line with en_US.UTF-8 UTF-8
gedit /etc/locale.gen
sudo locale-gen

#open terminal
