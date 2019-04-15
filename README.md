# webrato

[![Build Status](https://travis-ci.org/gitkent/webrato.svg?branch=master)](https://travis-ci.org/gitkent/webrato)
## Start up
### with Docker Compose
1. install Docker on your OS flavor
2. Clone the source
  ``` 
  git clone https://github.com/gitkent/webrato.git
  ```
3. Start app
  ```
  cd webrato
  docker-compose up
  ```
4. On your browser, go to should list out the existing data:
  ```
  http://localhost:8080/data/all
  ```
5. To add new entry, go to:
  ```
  http://localhost:8080/data/add?name=test&email=test@email.com
  ```