# README

```
rails new .
bundle install
gem install mysql2
```

```
# Install Capistrano, cap install STAGES=staging,production
cap install
```

```
# list all available tasks
$ bundle exec cap -T
```

**Check required files and directories exist**
```
cap staging deploy:check
```

```
cp config/deploy/staging.rb.example config/deploy/staging.rb
```

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
