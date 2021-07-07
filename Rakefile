# require 'pry'

task :environment do 
  require_relative "./config/environment"
end 

namespace :greeting do 
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'pone hola al terminal'
  task :hola do 
    puts "hola de Rake!"
  end 

  desc '把你好放入终端'
  task :你好 do 
    puts "你好我是Rake我想跟你爱爱"
  end 
end

# namespace :db do 
#   desc 'migrate changes to database'
#   task :migrate => environment do 
#     Student.create_table
#   end 
 

namespace :db do
  desc 'migrate changes to your database'
  task migrate: :environment do
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end 
end

desc 'drop into the Pry console'
task :console => :environment do 
  Pry.start
end 

