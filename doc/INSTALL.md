BC Web Shop extension INSTALL

Introduction
============

1. What is the BC Web Shop extension?
   ------------------------------------------------

   BC Web Shop is a simple eZ Publish extension
   that provides design and module of eZ Publish
   improved and tested for the needs of USA Customers.

   For more information about this extension please read the README file.

1. Copyright
   ---------

   BC Web Shop is copyright 1999 - 2023 Brookins Consulting, 1999 - 2015 eZ Systems AS.

   See: doc/COPYRIGHT for more information on the terms of the copyright and license

1.1. License
     -------

     BC Web Shop is licensed under the GNU General Public License.

     The complete license agreement is included in the doc/LICENSE file.

     BC Web Shop is free software: you can redistribute it and/or modify
     it under the terms of the GNU General Public License as published by
     the Free Software Foundation, version 2 of the License.

     BC Web Shop is distributed in the hope that it will be useful,
     but WITHOUT ANY WARRANTY; without even the implied warranty of
     MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
     GNU General Public License for more details.

     The GNU GPL gives you the right to use, modify and redistribute
     BC Web Shop under certain conditions. The GNU GPL license
     is distributed with the software, see the file doc/LICENSE.

     It is also available at http://www.gnu.org/licenses/gpl.txt

     You should have received a copy of the GNU General Public License
     along with BC Web Shop in doc/LICENSE.  If not, see http://www.gnu.org/licenses/.

     Using BC Web Shop under the terms of the GNU GPL is free (as in freedom).


2. Requirements
   ------------

   The following requirements exists for using BC Web Shop extension:

   o  eZ Publish version:

      Make sure you use eZ Publish version 5.x (required) or higher.

      Netgen eZ Publish Legacy 5.99.99alpha1 is recommended.

   o  PHP version:

      Make sure you have PHP 7.2 or higher.

      Tested with PHP 8.2.


Getting eZ Publish
==================

You can download a version of eZ Publish from https://github.com/netgen/ezpublish-legacy


Installing BC Web Shop extension
==========================================

1. Copy the extension files into the extension directory
   =====================================================

   Copy the package into the `extension' directory
   in the root of your eZ Publish installation.


2. Unpack the extension package files into the extension directory
   ===============================================================

   Unpack the files in the distribution. The command
   necessary is depends on the file you downloaded.

   [tar.gz]
   tar -zxvf bcwebshop.tar.gz

   [zip]
   unzip bcwebshop.tar.zip


3. (Optional) Git clone the latest GitHub brookinsconsulting bcwebshop extension sources into the extension directory
   ===============================================================

   You can optionaly fetch the latest extension source code from GitHub brookinsconsulting bcwebshop repository into the extension directory

cd /path/to/ezpublish;
cd extension;

mkdir bcwebshop;
cd bcwebshop;

git clone git@github.com:brookinsconsulting/bcwebshop.git . ;

sudo chmod -R 777 ../bcwebshop;


3.1. (Optional) Git download the latest GitHub brookinsconsulting bcwebshop extension sources into the extension directory
     ===============================================================

     You can optionaly fetch the latest extension source code from GitHub brookinsconsulting bcwebshop repository into the extension directory

cd /path/to/ezpublish;
cd extension;

mkdir bcwebshop
cd bcwebshop;

wget https://github.com/brookinsconsulting/bcwebshop/tarball/master;

or

wget https://github.com/brookinsconsulting/bcwebshop/zipball/master

tar -zxf brookinsconsulting-bcwebshop-d1d1411.tar.gz;

or

unzip brookinsconsulting-bcwebshop-d1d1411.tar.gz;

sudo chmod -R 777 ../bcwebshop;


3.5 Dependencies for BC Web Shop
   ===========================

BC Web Shop depends upon the following kernel override extension being installed and available:

- https://github.com/brookinsconsulting/bckernelmoduleoverride

We rely on this dependency to load the bcwebshop extension modules before the default kernel modules. This kernel override prevents kernel customizations or kernel hacking.


4. We must now enable the extension in eZ Publish.
   ===========================

   To do this edit site.ini.append(.php) in the folder
   /path/to/ezpublish/settings/override/. If this file does not exist;
   create it. Locate (or add) the block

   [ExtensionSettings] and add the line:
   ActiveExtensions[]=bcwebshop

   If you run several sites using only one distribution
   and only some of the sites should use the extension,
   make the changes in the override file of that siteaccess.

   E.g /path/to/ezpublish/settings/siteaccess/ezwebin_site_user/site.ini.append(.php)
   But instead of using ActiveExtensions you must add these lines instead:

   [ExtensionSettings]
   ActiveAccessExtensions[]=bcwebshop


5. Regenerate eZ Publish class autoloads
   ===========================

   You must regenerate autoloads for extension classes to be available via eZ Publish autoloads. This may mean running the following different commands.

cd /path/to/ezpublish;

php bin/php/ezpgenerateautoloads.php -v -e;

php bin/php/ezpgenerateautoloads.php -v -o;

#fin


6. There is no need to configure BC Web Shop extension after activation
   ===========================

   There are optional settings in settings/bcwebshop.ini mostly cronjob part and xml output specific.

   Create a settings override to customize these values. Review to understand extension features and options.


Usage
===========================

The complete extension usage documentation is included in the file doc/USAGE.


Use Cases
===========================

The complete extension usage documentation is included in the file doc/USECASES.


Troubleshooting
===============

1. Read the FAQ
   ------------

   Some problems are more common than others. The most common ones are listed
   in the the doc/FAQ.

2. Support
   -------

   If you have find any problems not handled by this document or the FAQ you
   can contact Brookins Consulting trough the support system:
   http://brookinsconsulting.com/contact
