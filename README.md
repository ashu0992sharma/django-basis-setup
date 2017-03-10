# django-basis-setup

This Project is for the first time setup of django.
It includes the basis requirements in requirements.txt

Pre-requisites:
1. Postgres setup (Referrence: https://www.digitalocean.com/community/tutorials/how-to-use-postgresql-with-your-django-application-on-ubuntu-14-04)

postgres setup steps:
			installation
				a. sudo apt-get install libpq-dev python-dev
				b. sudo apt-get install postgresql postgresql-contrib

			creating db and user
				a. sudo su - postgres
				b. createdb test
				c. createuser test --pwprompt (Please add "test" as password)

## Running celery servers(on local): ##
* RabbitMQ server setup Ubuntu:
      a. echo "deb http://www.rabbitmq.com/debian/ testing main" >> /etc/apt/sources.list
      b. curl http://www.rabbitmq.com/rabbitmq-signing-key-public.asc | sudo apt-key add -
      c. apt-get update
      d. sudo apt-get install rabbitmq-server
* RabbitMQ server setup Mac: https://www.rabbitmq.com/install-standalone-mac.html
* Running worker: celery -A webapp.conf.celery_app worker --loglevel=DEBUG
* Running beat server: celery beat -A webapp.conf.celery_app -l info

# Redis #
* To install Redis sudo apt-get install redis-server
* To start redis-server as a service sudo service redis-server start
* On Mac(*Installing: brew install redis   * Running server: redis-server)


## References: ##
* https://www.digitalocean.com/community/tutorials/how-to-install-and-manage-rabbitmq

Setup steps:
1. Clone or fork clone.
Please run: pip install -r requirements.txt
