# Getting Started

1. Clone this repo && `cd` into it
1. Run `cp .env.example .env`
1. Run `docker-compose up -d`

# Verify the Installation

After completing the **Getting Started** section, the following should work for you: 
1. Visit [http://localhost:9081](http://localhost:9081) to see the welcome page.
1. Connect to the mysql DB using these credentials: 
    1. host:        127.0.0.1
    1. port:        3311
    1. database:    db_admin_assignment
    1. username:    db_admin_assignment
    1. password:    secret
1. Verify that the SQL was imported
    1. Open a connection to the database using the credentials above.
    1. Ensure three tables exist: saccos, individiuals, transactions.
    1. Ensure that the transactions table has a few million rows in it.

If you made it this far, then you're good to start the live coding portion of the test.  

# Familiarize Yourself with the Database Tables

Take some time to read through the schema for each table. Think about whether there are any improvements you would make to them. 

# Write a Migration

Changes made to the database in a Laravel application require a database migration to be written. 

Read about [migrations here](https://laravel.com/docs/5.5/migrations) and practice implementing one or two migrations. You'll be asked to do this during the live-coding.

# Interacting with the Docker Container

The application is now running _within_ the docker container. There's a mysql container and an application container. These are basically computers within your computer.

To "get in" to the application container in order to run commands, you'll need to run this:

```bash
# - execute in an interactive terminal (-it)
# - on the db-admin-assignment-app container
# - the bash command (to open a prompt)
docker exec -it db-admin-assignment-app bash

# Now you can run whatever you like from within the container:
php artisan tinker
```
