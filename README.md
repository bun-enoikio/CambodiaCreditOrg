# CambodiaCreditOrg
about Cambodia Credit Org project
How to install project

in httpd-vhosts.conf add the following

<VirtualHost *:80>
    ServerName cco.local
    DocumentRoot /workspace/CambodiaCreditOrg/public
    SetEnv APPLICATION_ENV "development"
    <Directory /workspace/CambodiaCreditOrg/public>
       AllowOverride All
       Order allow,deny
       Allow from all
    </Directory>
</VirtualHost>

in hosts add the following

127.0.0.1       cco.local

if you are using PHP 5.4 or above, you can use the following cmd to start server

php -S 0.0.0.0:8080 -t public/ public/index.php
