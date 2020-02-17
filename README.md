# Drupal Project based on Lando
This is an attempt at a Lando-based development environment as an alternative to Bixal's docker-compose based
drupal-project

Requirements will be to cover the current feature set of drupal-project.

# ToDos
1. Figure out list of requirements
    1. Compare what drupal-project can do and what this will need to do
        1. Automated testing

# Getting Started
## Setting up a pre-existing project


## Creating a brand new project
This is below "Setting up a pre-existing project" because your'e probably going to be doing this less often.

# Patching
Sometimes you need to patch Drupal modules, themes, libraries, etc. Patches should be setup in the root level
composer.patches.json file. Any local patches should be added to the root level /patches directory.

# Testing
PHP Unit and Behat are installed for testing.

# Database access
PHPMyAdmin is installed, and you will see a link for it when running `lando start`; as the port will be randomly chosen,
you'll need to check that link for access.

If you wish to use a different tool for database access---such as [DataGrip](https://www.jetbrains.com/datagrip/) or
[Sequel Pro](https://www.sequelpro.com/)\--you set a port number to access it using `portforward` for the database
service in the `.lando.yml` file.
