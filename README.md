drupal_multisite_script
=======================

Bash script to automate multisite drupal creation.

Some stuff to take note of.

1.  Script is tailored for Ubuntu Servers.
2.  Drush is required to perform drupal related tasks.
3.  Utlizes a drupal multiple installation. Location of drupal folder is at /var/www/drupal7
4.  A vhost template file is included. Adjust according to your server settings.
5.  SFTP access is configure for each site. 1 Site = 1 Account = 1 SFTP Account.
6.  All site accounts folder at located within /home
7.  Database access is created with seperate login credentials per site. Install phpmyadmin to allow individual DB management.
8.  Email is triggered to specified email with all login details and credentials.
9.  Backup is located at /backup
10. Each site would have its own individual log folders.
11. Script utilizes a vhosts template "vhost-template-drupal". Change accordingly to fit your apache config.

Some congfig paramaters that requires changes
1. APACHE_ALL_VHOSTS : apache vhosts location
2. DRUPAL_FOLDER_PATH : drupal "sites" folder location
3. MYSQL_LOGIN : master mysql login name used to create individual db
4. MYSQL_PASS : password for above mentioned login
5. SERVER_URL : the url to to access phpmyamin / ftp
6. EMAIL_FROM : Notification email address of the sender
7. EMAIL_TO : Notification email address of the receiver
8. EMAIL_SUBJECT: Notification email subject.
9. EMAIL_CONTENT: Notification email contet. *the script itself is precoded with the ftp mysql login credentials


This is a script that i whipped out without putting much extended thought. It serves me well for my hosting my client's drupal sites
with access to the DB & FTP when needed. Alter it here and there and you would use it to host other open source platgorm as well.

Hope you guys enjoy it :)


