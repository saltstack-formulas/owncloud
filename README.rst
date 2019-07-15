owncloud
========

Install an owncloud instance on your server and/or client.

.. note::

    See the full `Salt Formulas installation and usage instructions
    <http://docs.saltstack.com/en/latest/topics/development/conventions/formulas.html>`_.

Available states
================

.. contents::
    :local:

``owncloud.client``
-------------------

Installs the Owncloud client package and service.

Includes:

- ``owncloud.repo``

``owncloud.repo``
-----------------

Configure the official Owncloud repository.
(Currently Debian(ish) only.)

``owncloud.server-full``
------------------------

Includes:

- ``owncloud.apache-php``
- ``owncloud.mysql-server``
- ``owncloud.mysql-client``
- ``owncloud.mysql``
- ``owncloud.server``
- ``owncloud.cron``

``owncloud.server``
-------------------

Installs the Owncloud server package and service.

``owncloud.mysql-server``
-------------------------

Installs a MySQL server.

If you need a more complex setup, please use the MySQL formula.

- https://github.com/saltstack-formulas/mysql-formula

``owncloud.mysql-client``
-------------------------

Installs a MySQL client.

If you need a more complex setup, please use the MySQL formula.

- https://github.com/saltstack-formulas/mysql-formula

``owncloud.mysql``
------------------

Sets up the user and configures a database.

If you need a more complex setup, please use the MySQL formula.

- https://github.com/saltstack-formulas/mysql-formula

``owncloud.apache-php``
-----------------------

Installs Apache2 web server and PHP7.

It's advisible to use the Apache2 and PHP formulas instead.
You'll need to configure Apache2 manually!

- https://github.com/saltstack-formulas/apache-formula
- https://github.com/saltstack-formulas/php-formula

``owncloud.cron``
-----------------

Installs a cron job to trigger background tasks.

See https://doc.owncloud.org/server/latest/admin_manual/configuration/server/background_jobs_configuration.html#cron

``owncloud.apcu``
-----------------

Installs the APCu PHP module, which provides in-memory caching.

See https://doc.owncloud.com/server/admin_manual/configuration/server/oc_server_tuning.html

This is only a minimalistic implementation of APCu for a vanilla Owncloud installation. If you need a more sophisticated configuration, please feel free to use a fully-fledged formula instead.

``owncloud.redis``
-----------------

Installs a minimalistic, local instance of Redis, which provides file locking.

See https://doc.owncloud.com/server/admin_manual/configuration/server/oc_server_tuning.html

This is only a minimalistic implementation of redis for a vanilla Owncloud installation. If you need a more sophisticated configuration, please feel free to use a fully-fledged formula like https://github.com/saltstack-formulas/redis-formula.
