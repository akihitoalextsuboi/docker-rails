# create rails file from Dockerfile & docker-compose.yml
1. docker-compose run web rails new . --force --database=postgresql
2. docker-compose build



3. replace the files with below
```
Replace the contents of config/database.yml with the following:

default: &default
  adapter: postgresql
  encoding: unicode
  host: db
  username: postgres
  password:
  pool: 5

development:
  <<: *default
  database: myapp_development


test:
  <<: *default
  database: myapp_test
```


4. docker-compose up
5. docker-compose run web rake db:create
6. look on the browser
if mac 
  http://localhost:3000
if windows
  http://192.168.99.100:3000

# stop
docker-compose down

# restart
docker-compose up

# login
docker-compose exec web bash
