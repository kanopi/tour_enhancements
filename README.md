# Tour Enhancements

CONTENTS OF THIS FILE
---------------------

 * Introduction
 * Requirements
 * Installation
 * Configuration
 * Maintainers


INTRODUCTION
------------

Additional routes and functionality for Tours.


REQUIREMENTS
------------

This module requires the following modules outside of Drupal core:

 * Drupal 8+ Core
 * Drupal 8+ Core Tour


INSTALLATION
------------

 * Install as you would normally install a contributed Drupal module. Visit:
   https://www.drupal.org/node/1897420 for further information.


CONFIGURATION
-------------

Adding Tours
* To add tours, you can add them in your custom module's config/optional folder
* Naming should be in the style tour.tour.unique-id.yml
* You can also add tours in the Drupal admin UI using the Tour UI module.  These tours are saved in the site config.

Configuring Tours
* You can add a tour to any route available in Drupal.
* A few routes allow for parameters.  Some example are:

All edit forms
entity.node.edit_form

Edit forms of a specific content type bundle
entity.node.edit_form
- bundle:how_to

All front end nodes
entity.node.canonical

A specific front end node
entity.node.canonical
- node:393469

Front end nodes of a specific content type bundle
entity.node.canonical
- bundle:how_to

MAINTAINERS
-----------

Current maintainers:
 * [thejimbirch](https://www.drupal.org/u/thejimbirch)

This project is supported by:
 * [Kanopi studios](https://www.drupal.org/kanopi-studios)
