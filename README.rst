**WARNING**: This repository is a fork of `Silex <https://github.com/silexphp/Silex>`_. While the original one is not maintained anymore and has been declared "end of life" in June 2018, this repository has been put up to date with Symfony 4.x (see branch) and 5.x (master) components.

Silex, a simple Web Framework
=============================

Silex is a PHP micro-framework to develop websites based on `Symfony
components`_:

.. code-block:: php

    <?php

    require_once __DIR__.'/../vendor/autoload.php';

    $app = new Silex\Application();

    $app->get('/hello/{name}', function ($name) use ($app) {
      return 'Hello '.$app->escape($name);
    });

    $app->run();

The current master works with PHP 7.2.5 or later, and Symfony 5.x.

Installation
------------

The recommended way to install Silex is through `Composer`_.
As this repository is not the main one and there are no releases, is has to be declared as follows in your composer.json:

.. code-block:: json
    "require": {
        ...
        "silex/silex": "dev-master",
        ...
    },

    "repositories": [
        ...
        {
          "type": "vcs",
          "url": "https://github.com/GregOriol/Silex"
        },
        ...
    ]

Then run:

.. code-block:: bash

    composer install


More Information
----------------

Read the `documentation`_ for more information.

Tests
-----

To run the test suite, you need `Composer`_ and `PHPUnit`_:

.. code-block:: bash

    composer install
    phpunit

Support
-------

If you have a configuration problem use the `silex tag`_ on StackOverflow to ask a question.

If you think there is an actual problem in Silex, please make a pull request.

Please note that this repository is mainly maintained for personnal use, so no support per se will be provided, but contributions are welcome!

License
-------

Silex is licensed under the MIT license.

.. _Symfony components: https://symfony.com
.. _Composer:           https://getcomposer.org
.. _PHPUnit:            https://phpunit.de
.. _documentation:      https://silex.symfony.com/documentation
.. _silex tag:          https://stackoverflow.com/questions/tagged/silex
