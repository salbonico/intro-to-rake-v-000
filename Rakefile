desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

task :environment do
  require_relative './config/environment'
end

namespace :db do
  desc "Migrate changes to your database"
  task :migrate => :environment do
    Student.create_table
  end

  desc "seed the database with dummy data"
  task :seed do
    require_relative './db/seeds.rb'
  end
end


  desc "Drop into the Pry console"
  task :console => :environment do
    Pry.start
  end
