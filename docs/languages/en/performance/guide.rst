.. _performance.guide:

Performance guide
=================

ZF2 comes along with a lot of possibilities to increase the performance of your application. 
We will cover here some best practices for it.

Autoloading
-------------------

If you have a stock ZF2 project, autoloading consumes a lot of time.
So this is one of the most importand parts to start when optimizing!

Composer
^^^^^^^^^^^^^
Try always to use composer if possible for vendor code.
Composer can generate an autoload classmap file, which will lower the time needed for autoloading files

Move to your root project directory and execute

.. code-block:: bash

    > composer install --optimize-autoloader
    
    [Alternative]
    > php composer.phar install -o
    
After this command you should see the generated classmap inside YOUR_PROJECT\vender\composer\autoload_classmap.php

