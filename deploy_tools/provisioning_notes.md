Provisioning a new site
=======================

## Required Packages:

* nginx
* Python 3
* Git
* pip
* virtaulenv
* gunicorn
* geckodriver
* selenium

eg, on Ubuntu:

    sudo apt-get install nginx git python3 python3-pip gunicorn
    sudo pip install virtualenv selenium
    wget https://github.com/mozilla/geckodriver/releases/download/v0.18.0/geckodriver-v0.18.0-linux64.tar.gz
    tar -xvzf geckodriver* 
    chmod +x geckodriver
    sudo mv geckodriver /usr/local/bin/

## Nginx Virtual Host config

* see nginx.template.conf
* replace SITENAME with, eg. staging.my-domain.com

## Upstart is no longer supported after Ubuntu 14.04, so use systemd

* see gunicorn-superlists-staging.service
* replace SITENAME with, gl staging.my-domain.com

## Folder structure:
Assume we have a user account at /home/usernanme

/home/username
|_ sites
    |_ SITENAME
        |_ database
        |_ source
        |_ static
        |_ virtualenv

