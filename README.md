cockroach-app
=============

The purpose of this repo is testing CockRoachDB 1.1 against PHP/Symfony/Doctrine.

```
vagrant up
vagrant ssh
cd /var/www
composer install
cockroach start --insecure --background
```

This will trigger [issue #3](https://github.com/radutopala/cockroach-app/issues/3): 
```
bin/console doctrine:schema:update -vvv
```
