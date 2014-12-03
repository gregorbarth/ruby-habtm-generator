#!/usr/bin/env rake
require "bundler/gem_tasks"
require 'rails/dummy/tasks'


task :clear do
  rm_rf 'spec/dummy'
end
task :test => [:clear, 'dummy:app'] do
  system 'rails g model user'
  system 'rails g model post'
  system 'rails g habtm user post'
  system 'rake db:migrate'
  system 'pwd'
  puts 'Running test'
  system 'rails r ../../test.rb'
end
