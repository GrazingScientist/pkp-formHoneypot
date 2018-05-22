# Form Honeypot anti-bot plugin for OJS

This plugin verifies new user registrations by creating a honeypot on the User Registration form.

## Requirements

* OJS 2.4.x
* PHP 5.3 or later

## Installation

Install this as a "generic" plugin in OJS.  To install manually via the filesystem, extract the contents of this archive to a directory (e.g. "formHoneypot") under "plugins/generic" in your OJS root.  To install via Git submodule, target that same directory path: `git submodule add https://github.com/ulsdevteam/pkp-formHoneypot plugins/generic/formHoneypot` and `git submodule update --init --recursive plugins/generic/formHoneypot`.  Run the upgrade script to register this plugin, e.g.: `php tools/upgrade.php upgrade`

## Configuration

You will need to select which field on the user registration form which you want to use as the honeypot.  This field will not be available on the form to regular users, but will be available within the user profile after registration.

## Usage

When a new user registers within a journal context, the field you select will be hidden by javascript.  A form submission which includes this field is assumed to be generated by a bot, and an error will be displayed.

## Author / License

Written by Clinton Graham for the [University of Pittsburgh](http://www.pitt.edu).  Copyright (c) University of Pittsburgh.

Released under a license of GPL v2 or later.
