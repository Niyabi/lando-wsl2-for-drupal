# lando-wsl2-for-drupal
Local developement environment for Drupal 9 based on Lando and WSL2.
Project is based on this **[article](https://www.liip.ch/en/blog/setup-drupal-and-lando-with-wsl2-on-windows)**.

## Requirements

* [WSL2](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
* [Ubuntu](https://www.microsoft.com/pl-pl/p/ubuntu/9nblggh4msv6)
* [Docker](https://www.docker.com/products/docker-desktop)
* [Lando](https://docs.lando.dev/)

Here is **[article](https://www.liip.ch/en/blog/setup-drupal-and-lando-with-wsl2-on-windows)** how to setup Lando inside WSL2 Ubuntu

## Drupal 9 installation
Go to *docroot* directory and install Drupal 9 using composer
```bash
lando start
lando composer create-project drupal/recommended-project ./
```

## Module instalation
Go to *docroot* directory and 
```bash
lando composer require drupal/module_name
```
e.g. lando composer require drupal/admin_toolbar

## Drush installation
To install drush run command
```bash
lando drush-install
```

## Drush
To use drush run command
```bash
lando drush your_command
``` 

## Commands
* Start / build lando
```bash
lando start
```
* Stop lando
```bash
lando stop
```
* Rebuild lando app
```bash
lando rebuild
```
* Destroy app (containers, databse, NOT FILES!)
```bash
lando destroy
```
* Import database
```bash
lando db-import path/to/file.sql
```
* Connect to container's shell 
```bash
lando ssh
```
* Enable xdebug
```bash
lando xdebug-on
```
* Disable xdebug
```bash
lando xdebug-off
```