source 'https://rubygems.org'

gem 'sinatra'
gem 'json'
gem 'oauth'

gem 'rails', github: 'rails/rails'
gem 'arel', github: 'rails/arel'
gem 'sqlite3'

group :development, :test do
  gem 'pry' # obviously don't do this in prod, just for demo purposes
end

group :production do
  gem 'ey_config'
  gem 'newrelic_rpm'
end

group :app_servers do
  gem 'puma', require: 'puma' # doesn't show up otherwise for some reason
  gem 'passenger', github: 'phusion/passenger'
  #gem 'passenger', '4.0.57'
  gem 'rhebok'
  platforms :ruby, :rbx do
    gem 'unicorn'
    gem 'thin'
  end
end
