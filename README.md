# create rails file from Dockerfile & docker-compose.yml
1. docker-compose run web rails new . --force
2. docker-compose build
3. docker-compose up
4. docker-compose run web rake db:create
5. look on the browser
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
