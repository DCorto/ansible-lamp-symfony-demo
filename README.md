# LAMP Vagrant Box with Ansible

This is for demo purposes only. Setups a LAMP Vagrant box with for work with a Symfony 3 fresh install.

## Ubuntu 14.04 LTS 
 
    - Apache 2.4
    - PHP 7.X
    - MySQL 5.5
    - Adminer Database management
    - Composer
    - Mailhog
 
## Usage

    - clone repo
    - vagrant up
    
    - browse to: http://192.168.100.99
    - browse to: http://192.168.100.99/email for send a test email ( check in Mailhog page )
    
       
    - for Adminer page, browse to: http://192.168.100.99/adminer
    - for Mailhog page, browse to: http://192.168.100.99:8025/
   
## Optional
    
Install the vagrant plugin vbguest with:
    
    vagrant plugin install vagrant-vbguest
    
More info: https://github.com/dotless-de/vagrant-vbguest    



