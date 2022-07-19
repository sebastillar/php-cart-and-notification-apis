# CartApi and Notification Engine platform
This is the main repository with submodules which includes:
* a CartAPI project 
* a container with Laravel and Lucid arch scaffolding to develop a Notification Engine
* OpenApi spec for CartApi

## Docker-Composer Services

* CartAPI
- service name: cart-api
- Mapped ports: 6000:8000

* MYSQL DB
- service name: db
- Mapped ports: 3308:3306

* Notification Engine
- service name: notification-engine
- Mapped ports: 6001:8000


## Getting started
1. `git clone git@github.com:sebastillar/php-cart-and-notification-apis.git --recurse-submodules`

2. `cp .env.example .env`


3. git submodule foreach 'git checkout develop && git pull && cp -n .env.excample .env'

4. docker-compose up -d --build

5. npm install

6. Commands to access cart-api container:
- docker-compose exec cart-api /bin/bash
or for run migrations:
- docker-compose exec cart-api php artisan migrate
