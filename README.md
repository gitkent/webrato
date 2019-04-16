# webrato

[![Build Status](https://travis-ci.com/gitkent/webrato.svg?branch=master)](https://travis-ci.com/gitkent/webrato)
## Intro
This is a simple springboot apo query to MySQL database to get a list of users. The database is pre-loaded with some data and you can add more data(user) into the database by calling `/data/add` API. The `MYSQL_ROOT_PASSWORD`, `MYSQL_PASSWORD`, and `DB_PASSWORD` are epehmeral. You can use any password you want to startup the app. 

## Start up
### with Docker Compose
1. install Docker on your OS flavor
2. Clone the source
  ``` 
  git clone https://github.com/gitkent/webrato.git
  ```
3. Start app on linux
  ```
  export MYSQL_ROOT_PASSWORD=myrootpass
  export MYSQL_PASSWORD=mydbpass
  export DB_PASSWORD=$MYSQL_PASSWORD

  cd webrato
  docker-compose up --build
  ```
4. On your browser, go to should list out the existing data:
  ```
  http://localhost:8080/data/all
  ```
5. To add new entry, go to:
  ```
  http://localhost:8080/data/add?name=test&email=test@email.com
  ```

## Envrionment variables
| Name | Default | Required? | Description |
|:-----|:--------|:---------:|:------------|
|MYSQL_ROOT_PASSWORD|<none>|Yes|Set you own MySQL root password
|MYSQL_PASSWORD|<none>|Yes|Set your own MySQL database password
|DB_PASSWORD|<none>|Yes|This will be picked up by the Springboot App. Set this to the same as `$MYSQL_PASSWORD`

## Limitations
- use HTTPS
- unit testing to test `/data/all` and `/data/add` functions
- setup authentication (e.g. oauth)
- test to cover multiple openjdk versions