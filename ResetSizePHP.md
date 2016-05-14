##how to change the max import size in php##

###*Find php.ini that is associated with your wordpress website*###

- Create new text file in our wp-admin directory root and name it info.php.
- Open info.php and add these lines:
	
	<?php
	
	phpinfo();
	
	?>
- save it
- Go to yourwebsitename(probably localhost)/wp-admin/info.php in any web-browser.
- In the 8th line you will see: Configuration File (php.ini) Path
- In the 9th line you will see: Loaded Configuration File
- So you can find your php.ini page that is associated with your wordpress web-site.

###*Editing the php.ini to allow larger database uploads*###

- Login into your cPanel.
- Copy your php.ini from your main domain to your subdomain document root folder.
- Edit the php.ini you copied to your subdomain for your PhpMyAdmin.
- Change the following to be larger than 100MB. You can make the settings like the example below.
	- upload_max_filesize = 200M
	- memory_limit = 512M
	- post_max_size = 200M
	- Save the file.
- Make the php.ini recursive in the .htaccess by editing the .htaccess in the subdomain directory and adding the path to your subdomain document root folder.

That's all there is to it. You will now be able to use your Softaculous installed PhpMyAdmin to upload a database larger than 50mb.