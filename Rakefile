require 'rake'
require 'rubygems'
require 'rake/testtask'
require 'rdoc/task'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gemspec|
    gemspec.name = "auto_migration"
    gemspec.summary = "Auto database migration."
    gemspec.description = "Auto database migration."
    gemspec.email = "rubyer1993@gmail.com"
    gemspec.homepage = "https://github.com/sai1024/auto_migrations"
    gemspec.authors = ["sai (originally by PJ Hyett)"]
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler not available. Install it with: sudo gem install jeweler -s http://gemcutter.org"
end

desc 'Default: run unit tests.'
task :default => :test

desc 'Test the auto_migrations plugin.'
Rake::TestTask.new(:test) do |t|
  t.libs << 'lib'
  t.pattern = 'test/**/*_test.rb'
  t.verbose = true
end

desc 'Generate documentation for the auto_migrations plugin.'
Rake::RDocTask.new(:rdoc) do |rdoc|
  files = ['README', 'LICENSE', 'lib/**/*.rb']
  rdoc.rdoc_files.add(files)
  rdoc.main = "README" # page to start on
  rdoc.title = "auto_migrations"
  rdoc.template = File.exists?(t="/Users/chris/ruby/projects/err/rock/template.rb") ? t : "/var/www/rock/template.rb"
  rdoc.rdoc_dir = 'doc' # rdoc output folder
  rdoc.options << '--inline-source'
end
