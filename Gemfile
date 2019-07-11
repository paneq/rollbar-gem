# This file was generated by Appraisal

source 'https://rubygems.org'

# Used by spec/commands/rollbar_rails_runner_spec, and can be used whenever a
# new process is created during tests. (Testing rake tasks, for example.)
# This is a workaround for ENV['BUNDLE_GEMFILE'] not working as expected on Travis.
# We use the ||= assignment because Travis loads the gemfile twice, the second time
# with the wrong gemfile path.
ENV['CURRENT_GEMFILE'] ||= __FILE__

is_jruby = defined?(JRUBY_VERSION) || (defined?(RUBY_ENGINE) && RUBY_ENGINE == 'jruby')

GEMFILE_RAILS_VERSION = '6.0.0rc1'.freeze

gem 'activerecord-jdbcsqlite3-adapter', :platform => :jruby
gem 'appraisal'
gem 'jruby-openssl', :platform => :jruby
gem 'rails', GEMFILE_RAILS_VERSION
gem 'rake'
if GEMFILE_RAILS_VERSION < '6.0'
  gem 'rspec-rails', '~> 3.4'
else
  # TODO: update this when 4.x becomes available on Rubygems
  gem 'rspec-rails', :git => 'https://github.com/rspec/rspec-rails', :ref => 'v4.0.0.beta2' # rubocop:disable Bundler/DuplicatedGem
end

if GEMFILE_RAILS_VERSION < '6.0'
  gem 'sqlite3', '< 1.4.0', :platform => [:ruby, :mswin, :mingw]
else
  gem 'sqlite3', '~> 1.4', :platform => [:ruby, :mswin, :mingw] # rubocop:disable Bundler/DuplicatedGem
end

if RUBY_VERSION < '2.2.2'
  gem 'sidekiq', '~> 2.13.0'
else
  gem 'sidekiq', '>= 2.13.0' # rubocop:disable Bundler/DuplicatedGem
end

platforms :rbx do
  gem 'minitest'
  gem 'racc'
  gem 'rubinius-developer_tools'
  gem 'rubysl', '~> 2.0' unless RUBY_VERSION.start_with?('1')
end

if RUBY_VERSION.start_with?('1.9')
  gem 'capistrano', '<= 3.4.1', :require => false
  gem 'shoryuken', '>= 4.0.0', '<= 4.0.2'
  gem 'sucker_punch', '~> 1.0'
elsif RUBY_VERSION.start_with?('2')
  gem 'capistrano', :require => false # rubocop:disable Bundler/DuplicatedGem
  gem 'codacy-coverage'
  gem 'shoryuken' # rubocop:disable Bundler/DuplicatedGem
  gem 'simplecov'
  gem 'sucker_punch', '~> 2.0' # rubocop:disable Bundler/DuplicatedGem
end

unless is_jruby
  # JRuby doesn't support fork, which is required for this test helper.
  gem 'rspec-command'
end

gem 'aws-sdk-sqs'
gem 'database_cleaner'
if GEMFILE_RAILS_VERSION < '6.0'
  gem 'delayed_job', :require => false
else
  gem 'delayed_job', '~> 4.1', :require => false # rubocop:disable Bundler/DuplicatedGem
end
gem 'generator_spec'
gem 'girl_friday', '>= 0.11.1'
gem 'redis'
gem 'resque', '< 2.0.0'
gem 'rubocop', :require => false
gem 'sinatra'
gem 'webmock', :require => false
gemspec
