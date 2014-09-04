Rails Protocol
==============

A guide for writing great web apps.

Set Up Laptop
-------------

Recommend using [RVM] to manage ruby versions and installing [Rubocop] to
perform code style checking.

[RVM]: http://rvm.io
[Rubocop]: https://github.com/bbatsov/rubocop

Create and Setup App
--------------------

Clone the repository and run `rake db:migrate` to set up the database
and `rake` to run the test suite.

Use `.env` file to hold configuration details (e.g. secret credentials).
Do not check this into Git.

Create a `.env.example` file with example configuration details. Check this into Git.

Use the Rails `secrets.yml` to reference the ENV variables.

Git Protocol
------------

Follow the normal [Git Protocol](/protocol/git).

Code Review
-----------

Follow the normal [Code Review guidelines](/code-review). When reviewing others'
Rails work, look in particular for:

* Review data integrity closely, such as migrations that make irreversible
  changes to the data, and whether there is a related todo to make a database
  backup during the staging and production deploys.
* Review SQL queries for potential SQL injection.
* Review whether dependency upgrades include a reason in the commit message,
  such as a link to the dependency's `ChangeLog` or `NEWS` file.
* Review whether new database indexes are necessary if new columns or SQL
  queries were added.
* Review whether new scheduler (`cron`) tasks have been added and whether there
  is a related todo in the project management system to add it during the
  staging and production deploys.

Deploy
------

Semaphore will deploy to Heroku automatically when changes have been merged
into the master branch.

