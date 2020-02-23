# Drupal Project based on Lando
This is an attempt at a [Lando](https://docs.lando.dev/basics/)\-based development environment as an alternative to Bixal's docker-compose based
drupal-project.

Requirements will be to cover the current feature set of drupal-project.

# ToDos
1. Figure out list of requirements
    1. Compare what drupal-project can do and what this will need to do
        1. Automated testing

# Getting Started
## Requirements
- Docker
- Lando
- Composer (recommended, but not required)

## Setting up a pre-existing project
1. Open a terminal
1. Navigate to the root directory of this project
1. Type `lando start` and hit enter

## Creating a brand new project
This is below "Setting up a pre-existing project" because your'e probably going to be doing this less often.

# Patching
Sometimes you need to patch Drupal modules, themes, libraries, etc. Patches should be setup in the root level
`composer.patches.json` file. Any local patches should be added to the root level `/patches` directory.

# Testing
PHP Unit and Behat are installed for testing.

# Database access
PHPMyAdmin is installed, and you will see a link for it when running `lando start`. The easiest access for this to go to
https://db-drupal-site.lndo.site

If you wish to use a different tool for database access---such as [DataGrip](https://www.jetbrains.com/datagrip/) or
[Sequel Pro](https://www.sequelpro.com/)\--you set a port number to access it using `portforward` for the database
service in the `.lando.yml` file.

# Mail
MailHog is setup so you can test the email sending capability of the site. You can visit the MailHog server at
mail-drupal-site.lndo.site

# Destroying your project
Sometimes you may want to completely destroy your project, meaning to delete all the related containers. This is done
with:

- `lando destroy`

This, again, will delete all of your containers and volumes, meaning your database will be gone. All the project files
will remain though.
