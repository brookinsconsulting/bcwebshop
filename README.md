BC Web Shop
========================

bcwebshop is the eZ Publish webshop module views within a separate extension providing for greater customization of the base web shop solution.

- Git Repository and Source code: http://github.com/brookinsconsulting/bcwebshop


Requirements
============

This extension is now compatible and tested with eZ Publish 5.x+ (Legacy) and PHP 8.2.3

Tested with Netgen eZ Publish Legacy 5.99.99alpha1

Ini Settings
---------

This solution depends on this extension being loaded in your settings/override/site.ini.append.php

[ExtensionSettings]
ActiveExtensions[]
ActiveExtensions[]=bcwebshop


Autoloads
---------

This solution depends on autoloads to function

To use this solution you must first regenerate autoloads for your installation

php ./bin/php/ezpgenerateautoloads.php -e;

Kernel Override Autoloads
---------

This script depends on kernel override autoloads to function

To use this solution you must first regenerate autoloads for your installation

php ./bin/php/ezpgenerateautoloads.php -o;


Usage
===========================

The complete extension usage documentation is included in the file doc/USAGE.


CREDITS
=======

The complete extension credits documentation is included in the file doc/CREDITS.


Troubleshooting
===============

1. Read the FAQ
   ------------

   Some problems are more common than others. The most common ones
   are listed in the the doc/FAQ.

2. Support
   -------

   If you have find any problems not handled by this document or the FAQ you
   can contact Brookins Consulting through the support system:
   http://brookinsconsulting.com/contact