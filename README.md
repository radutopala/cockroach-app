cockroach-app
=============

```
vagrant up
vagrant ssh
cd /var/www
composer install
```

This will trigger issue#1: 
```
bin/console doctrine:database:create -vvv
```

If you move to branch issue_1 and run:
```
bin/console doctrine:schema:update -vvv
```
will trigger issue#2.
