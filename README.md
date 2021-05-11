## Simple docker config for laravel.
It use nginx(alpine) ,mySql, php(alpine), composer, npm(node alpine) & artisan(laravel).

### Setup :

* first change docker services versions to your own version in Dockerfile & docker-compose.yml.
* To start use : "docker-compose up -d --build"
* To end progresss use : "docker-compose down"
* To run commands (here npm and artisan commands) use : "docker-compose run --rm <related-command>"

* command to install laravel in "/src" : "docker-compose run --rm composer create-project laravel/laravel ."
* change laravel storage folder permissions while development(linux/ubuntu preferred) : "sudo chmod -R 777"
* setup mySql service data from docker-compose.yml in laravel .env file
* use "sudo service mysql stop" while error in "docker-compose up -d" in linux/ubuntu

#### attention : in case of not running nginx container, use "docker-compose down" & better to stop simillar containers and ports to checkout the errors.
