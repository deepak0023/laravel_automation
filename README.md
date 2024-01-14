# laravel_automation
This repository is used to understand about the laravel automation

## Docker Setup

#### The present setup is for dev environment , for production environment remove the bind volumes from the source folder

#### Update db connection in src/.env to the following
```
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=homestaed
DB_USERNAME=homestaed
DB_PASSWORD=secret
```

#### Run the below commmand to have an up and running laravel project with docker and external images
```
sudo docker-compose up -d
```
Since all the services/jobs are in the same docker-compose, they are in the same network

#### To see the runng laravel application visit the below URL
```
http://localhost:8000/
```
Now you can make changes in the code and it will reflect in the UI
#### To check the docker container status use
```
sudo docker ps -a
```
#### To check the docker images
```
sudo docker images
```
#### To rebuild specific images after changing docker related files
```
sudo docker-compose up -d -build <space seperated service/job names defined in docker-compose>
```
#### To rebuild specific conatainers
```
sudo docker-compose up -d <space seperated service/job names defined in docker-compose>
```
#### To migrate table use
```
sudo docker-compose run --rm artisan migrate
```
#### To install new package use
```
sudo docker-compose run --rm composer install <package-name>
```
#### To stop the containers use the follwing command
```
sudo docker-compose down
```

