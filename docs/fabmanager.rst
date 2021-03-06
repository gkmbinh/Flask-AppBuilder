Command Line Manager
====================

Since version 1.3.0 F.A.B. has a command line manager, you can use it for many development tasks.
Many of the commands are design to import **AppBuilder** class initialized by your application.
By default it will assume your application follows the skeleton structure, so it will try to import
appbuilder from *app/__init__.py*. You can pass your own info to where appbuilder is being initialized.

Take a quick look to the current possibilities. The bold ones require your appbuilder.

  - babel-compile - Babel, Compiles all translations

  - babel-extract - Babel, Extracts and updates all messages.

  - **create-admin** - Creates an admin user

  - create-app - Create a Skeleton application (SQLAlchemy or MongoEngine).

  - **create-db** - Create all your database objects (SQLAlchemy only)

  - **list-users** - List all users on the database.

  - **list-views** - List all registered views.

  - **reset-password** - Resets a user's password.

  - **run** - Runs Flask dev web server.

  - **security-cleanup** - Cleanup unused permissions from views and roles.

  - **upgrade-db** - Upgrade your database after F.A.B upgrade.

  - **version** - Flask-AppBuilder package version.

Command Line uses the excelent click package, so you can have a detailed help for each command, for instance::

    $ fabmanager create-app --help
    Usage: fabmanager create-app [OPTIONS]

    Create a Skeleton application

    Options:
    --name TEXT                     Your application name, directory will have
                                  this name
    -engine [SQLAlchemy|MongoEngine]
                                  Write your engine type
    --help                          Show this message and exit.


**create-app** - Create new Applications
----------------------------------------

To create a ready to dev skeleton application, you can use this command for SQLAlchemy engine and MongoEngine (MongoDB).
This commands needs an internet connection to **github.com**, because it will download a zip version of the skeleton repos.

**create-admin** - Create an admin user
---------------------------------------

Use this to create your first **Admin** user, or additional ones. issue on the root directory of your application
if your initializing **AppBuilder** on *app/__init__.py* and have named it appbuilder. If not use the **--app** and
**--appbuilder** switches to identify how to import **appbuilder**.

This admin user can be used to any type of authentication method configured, but *fabmanager* will not checkit so
it will allways ask for a password (assumes AUTH_DB).

**upgrade-db** - Upgrade your database after F.A.B. upgrade to 1.3.0
--------------------------------------------------------------------

Will upgrade your database, necessary if your already using F.A.B. Users now are able to have multiple roles.
Take a look at :doc:`versionmigration`

Issue on the root directory of your application
if your initializing **AppBuilder** on app/__init__.py and have named it appbuilder. If not use the **--app** and
**--appbuilder** switches to identify how to import **appbuilder**.

**reset-password** - Resets a user's password.
----------------------------------------------

Reset a user's password, also needs to import **appbuilder** so 
Issue on the root directory of your application
if your initializing **AppBuilder** on app/__init__.py and have named it appbuilder. If not use the **--app** and
**--appbuilder** switches to identify how to import **appbuilder**.


