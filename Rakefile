ENV["SINATRA_ENV"] ||= "development"

require_relative './config/environment'
require 'sinatra/activerecord/rake'
require './app/controllers/application_controller'

# Type `rake -T` on your command line to see the available rake tasks.

task :console do
  Pry.start
end

task :migrations do
  puts "migrating databases..."
  system("rake db:migrate && rake db:migrate SINATRA_ENV=test")
end