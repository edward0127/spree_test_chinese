# README

This README would normally document whatever steps are necessary to get the
application up and running.

First time to run:

docker-compose build --rm
docker-compose run --rm web bundle exec rails g spree:install --user_class=Spree::User
docker-compose run --rm web bundle exec rails g spree:auth:install
docker-compose run --rm web bundle exec rails g spree_gateway:install
docker-compose run --rm web bundle exec rails webpacker:install
docker-compose run --rm web bundle exec rake db:migrate assets:precompile
docker-compose up

docker-compose run --rm web RAILS_ENV=production rails c

Later on:

docker-compose builddocker-compose up


Clean all docker file:

docker system prune -a --volumes

delete .babelrc if Cannot find module 'babel-plugin-syntax-dynamic-import'

RAILS_ENV=production bundle exec rails g spree:install --user_class=Spree::User
RAILS_ENV=production bundle exec rails g spree:auth:install
RAILS_ENV=production bundle exec rails g spree_gateway:install
RAILS_ENV=production bundle exec rails webpacker:install
RAILS_ENV=production bundle exec rake db:migrate assets:precompile

docker-compose run --rm web rails c