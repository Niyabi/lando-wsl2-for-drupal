# lando-wsl2-for-drupal
Local developement environment for Drupal 9 based on Lando and WSL2

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
Just run (e.g. lando module drupal/admin_toolbar)
```bash
lando module drupal/module_name
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