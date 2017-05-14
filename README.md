cockroach-app
=============

The purpose of this repo is testing CockRoachDB 1.0 against PHP/Symfony/Doctrine.

```
vagrant up
vagrant ssh
cd /var/www
composer install
```

This will trigger [issue #1](https://github.com/radutopala/cockroach-app/issues/1): 
```
bin/console doctrine:database:create -vvv
```

If you move to branch issue_1 and run:
```
bin/console doctrine:schema:update -vvv
```
will trigger [issue #2](https://github.com/radutopala/cockroach-app/issues/2).
