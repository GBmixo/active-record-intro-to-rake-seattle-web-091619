namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

task :environment do
  require_relative './config/environment'
end
 

desc 'console'
task :console => :environment do
end

namespace :db do
  desc 'creates students table in database'
  task :migrate => :environment do
    Student.create_table
  end
  desc 'seeds the database with dummy data from a seed file'
  task :seed => :environment do
    require_relative './db/seeds.rb'
  end
end