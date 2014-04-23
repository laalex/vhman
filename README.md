vhman
=====

Small shell program to manage the VHOSTS for *apache 2.4*

RUN THIS AS ROOT
================

To use this you first need to download vhman file into any directory and then update file permissions as follows:
_chmod u+x vhman

To use the file, you can call it like it follows:
`./vhman create host_name config_name www_dir_name`

For example: 
`./vhman create somewebsite.local somewebsite www_for_website`
After executing the above command, a virtual host can be accessed via `http://somewebsite.local` and will have it's root into /var/www/www_for_website. Also the configuration file `somewebsite.conf` will be created within /sites-available/ and /sites-enabled/ folders from apache.


Also you can remove a virtual host by usig 
`./vhman delete host_name config_name www_dir_name`
For example you can use:
`./vhman delete somewebsite.local somewebsite www_for_website`

You can obtain those information by typing `./vhman help` into your console. 

*Also, if you have different location for apache2.4 feel free to change those lines in the file (8-11):*

email='roshkattu94@gmail.com'
sitesEnable='/etc/apache2/sites-enabled/'
sitesAvailable='/etc/apache2/sites-available/'
userDir='/var/www/'

_Feel free to use it however you want._ 