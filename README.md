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

 * Install as you would normally install a contributed Drupal module. Visit
   https://www.drupal.org/node/1897420 for further information.


CONFIGURATION
-------------

* Adding Tours

  - To add tours, add them in your custom module's config/optional folder

  - Naming should be in the style tour.tour.unique-id.yml

  - You can also add tours in the Drupal admin UI using the Tour UI module.
    These tours are saved in the site config.

* Configuring Tours

  - You can add a tour to any route available in Drupal.

  - A few routes allow for parameters.  Some example are:

    - *All edit forms*
      `entity.node.edit_form`

    - *Edit forms of a specific content type bundle*
      `entity.node.edit_form`
      `- bundle:how_to`

    - *All front end nodes*
      `entity.node.canonical`

    - *A specific front end node*
      `entity.node.canonical`
      `- node:393469`

    - *Front end nodes of a specific content type bundle*
      `entity.node.canonical`
      `- bundle:how_to`

* Adding additional route parameters

  - The primary hook of this module, `tour_enhancements_page_bottom`  in
    tour_enhancements.module adds the availability of "bundle" type to
    entity.node.canonical, so you can add tours to all article nodes.  You can
    also add additional if statements around line 33 to check for things like
    if it has a certain field, or if it is published.

* Viewing Tours

  - If the user has the permission to view the Admin Toolbar, and the permission
    to view tours, a button will appear in the top right of the toolbar.

  - Tours can also be viewed to those with permissions to view tours by adding
    the `?tour` parameter to the url the tour should appear on based on the
    route.

MAINTAINERS
-----------

Current maintainers:
 * [thejimbirch](https://www.drupal.org/u/thejimbirch)

This project is supported by:
 * [Kanopi studios](https://www.drupal.org/kanopi-studios)
