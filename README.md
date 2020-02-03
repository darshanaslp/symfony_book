Installation Guide

Download the source code from git lab

Run below command setup the project dependencies

`composer install`

Update the parameters.yml in app/config with below values
 
database_host: 127.0.0.1 
database_port: 3306 
database_name: BookStore 
database_user: root 
database_password: 
mailer_transport: smtp 
mailer_host: smtp.mailtrap.io 
mailer_user: null 
mailer_password: null
secret: 8PWLg7c2U

You can Easily import bookstore.sql file to database

and run the below command 

`php bin/console server:run`

or

Run below command to create the tables

`php bin/console doctrine:schema:update –-force`

un below command to load the migration scripts 

`php bin/console doctrine:migrations:migrate`

Run below command to seed the database 

`php bin/console doctrine:fixtures:load`

Finally to load the application run the below command 

`php bin/console server:run`

Now the application should be available under http://localhost:8000/ 
Login username: admin
Login password: p@ssword

To run the Test cases (Unit & Functional) run the below commands

Functional > `./vendor/bin/simple-phpunit tests/AppBundle/Controller/ `

Unit > `./vendor/bin/simple-phpunit tests/AppBundle/Utils`

 if you get any permission issue clear the cache `php bin/console cache:clear --env=prod`
