require 'rake/testtask'
require 'find'

desc 'Say hello'
task :hello do
  puts "Hello there. This is the 'hello' task."
end

desc 'Te Amo'
task :amo do
  puts "Fiesta! Fiesta!　情熱を解き放とう！"
end

desc 'Run tests'
task :default => :test

Rake::TestTask.new(:test) do |task|
  task.libs << "test"
  task.libs << "lib"
  task.test_files = FileList['test/**/*_test.rb']
end

desc 'Display all files inventory'
task :inventory do
  Find.find('.') do |name|
    next if name.include?('/.')
    puts name if File.file?(name)
  end
end


# desc 'Run Tests'
# task :test do
#   sh 'ruby ./test/todolist_project_test.rb'
# end
