# Dokerize Wordpress application

**Contains:**
- Nginx
- php7
- MySQL
- NodeJs

## Run wordpress app in Docker containers:

1. 
    Clone this repo

2. 
    Go to the cloned folder
    ```bash
    cd docker-wordpress
    ```
3.
    Create new empty folder (by default this folder must call 'app'. But if project folder have different name, you must change APP_DIR variable in docker/.env file to actual folder name. For example, `APP_DIR=../other_folder_name/`) and put you app in this folder.
    
4.
    Go to the folder named 'docker' 
    ```bash
    cd docker
    ```
5. 
    Up the containers
    ```bash
    docker-compose up -d --build
    ```
6. 
    Yor project available in http://localhost/

Run commands (examlple)
NodeJs:
```bash
docker-compose run node yarn add ...
```
Composer:
```bash
docker-compose run composer install
```

### Other links:
* phpMyAdmin http://localhost:8080/

After up the containers, a 'data' folder will appear in the 'docker-symfony' folder, which contains logs, elasticsearch indices and a database.
