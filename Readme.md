## HOW TO SETUP YOUR LOCAL WITH NEW PROJECT
- Clone the project to your local machine
- Inside the root DIR run `docker-compose up`
- Navigate to your localhost ex: http://localhost:8000/

## HOW TO SETUP YOUR LOCAL WITH EXISTING PROJECT
- Create a folder named new_db on root DIR
- Place the live database there and rename the file to starter_db.sql, it will be copied over to the local instance automatically

- Create a folder named db_data on root DIR.
- The docker mysql database instance volume will be created there automatically.

- Copy over the live files to my_site folder in root DIR
- The folder name should be my_site and the WP files needs to be under public folder

- Make sure you have docker running locally
- run `docker-compose up` 

- Please follow this one-time step
   - Navigate to http://localhost:8080/ and login using phpMyAdmin container credentials listed below
   - Navigate into the `wordpress` database and open `wp_options` table
   - Change the `siteurl` and `home` to your localhost address.
   ex: http://localhost:8000/

### phpMyAdmin container

- Navigate to http://localhost:8080/
- use username `wordpress` and password `wordpress`

### MYSQL container

- To SSH into database from the container; 
  - `docker-compose exec db bash` 
  - From inside the container `mysql -u wordpress -p`

### WordPress container

- Navigate to http://localhost:8000/
- `docker-compose exec wordpress bash` 
