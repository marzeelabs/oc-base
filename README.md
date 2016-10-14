# Open Consortium 8.x project template

<!-- [![Build Status](https://travis-ci.org/drupalcommerce/project-base.svg?branch=8.x)](https://travis-ci.org/drupalcommerce/project-base) -->

Use [Composer](https://getcomposer.org/) to get Drupal + Open Consortium 8.x with all dependencies.

Based on [drupal-composer/drupal-project](https://github.com/drupal-composer/drupal-project).

## Usage

First you need to [install composer](https://getcomposer.org/doc/00-intro.md#installation-linux-unix-osx).

> Note: The instructions below refer to the [global composer installation](https://getcomposer.org/doc/00-intro.md#globally).
You might need to replace `composer` with `php composer.phar` (or similar)
for your setup.

After that clone this repository (request private access to https://github.com/marzeelabs/oc) and run

```
composer install
```

Done! You should create a new git repository, and commit all files not excluded by the .gitignore file.

## What does the template do?

* Drupal is installed in the `web` directory.
* Modules (packages of type `drupal-module`) are placed in `web/modules/contrib/`
* Theme (packages of type `drupal-theme`) are placed in `web/themes/contrib/`
* Profiles (packages of type `drupal-profile`) are placed in `web/profiles/`
* Creates default writable versions of `settings.php` and `services.yml`.
* Creates the `sites/default/files` directory.

## Re-using Phing 

You can re-use the Phing commands from the OC profile or include them in your custom `build.xml`.

For example to install the site, you would run

```
vendor/bin/phing -f web/profiles/oc/build.xml install
```

You probably need to create a custom `web/profiles/oc/build.properties` that looks like

```
project.basedir = THIS-DIRECTORY
drush.cmd = THIS-DIRECTORY/vendor/bin/drush
```

## Updating Open Consortium

TODO
