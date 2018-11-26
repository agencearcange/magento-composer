# Magento 1.9 based to composer #

This is simple a skeleton repo for a WordPress site managed by composer.phar.

## Specifications

* Public folder for your web server : `public`
* Patch for php 7.2 included
* Symfony web server included for development


Tested with :

* Magento 1.9.*
* Magento single / multi website

## Getting Started

1. Create a new mysql database.
2. Use `composer install` cmd.
3. Create your own local.xml
4. Add any required plugins, from their [firegento](http://packages.firegento.com/) packages
5. Launch your local server with `php bin/console server:start`

#### Development

**> Get magento and packages**

```
composer install
```
![composer install cmd](https://i.imgur.com/YUGvKoW.png)

**> Set url**

Change `web/secure/base_url` and `web/unsecure/base_url` to http://localhost:8000/ into `core_config_data` table

**> Launch your local server**

```
$ php bin/console server:start
```

#### Production

**> Get magento and packages and optimize composer**

```
composer install --no-dev --prefer-dist --no-interaction --optimize-autoloader
```

**> Set url**

Change `web/secure/base_url` and `web/unsecure/base_url` to http[s]://yourwebsite/ into `core_config_data` table

**> Send to your prod server via FTP or with your favorite deployment tool :thumbsup:**

## Contribution

 You can fork it and submit your change with a pull request !