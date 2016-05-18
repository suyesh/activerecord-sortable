source 'https://rubygems.org'

rails_version = ENV['RAILS_VERSION'] || '>= 3.0'
gem 'rails', rails_version
if ENV['RAILS_VERSION'] == '~> 3.2.0' && (RUBY_VERSION == '1.9.3' || defined?(JRUBY_VERSION))
  gem 'rack-cache', '1.2'
end
gem 'jquery-rails'
gem 'jquery-ui-rails'

if RUBY_VERSION == '1.9.3' || defined?(JRUBY_VERSION)
  gem 'mime-types', '2.6.2'
end

if defined?(JRUBY_VERSION)
  gem 'activerecord-jdbcsqlite3-adapter'
else
  gem 'sqlite3'

  if defined?(RUBY_VERSION) && RUBY_VERSION == '2.2.0' && ['~> 3.2.0', '~> 4.0.0'].include?(ENV['RAILS_VERSION'])
    gem 'rubysl-test-unit'
  end
end

if defined?(RUBY_VERSION) && RUBY_VERSION == '2.2.0' && ENV['RAILS_VERSION'] == '~> 3.2.0'
  gem 'rspec-rails', '3.3.0'
else
  gem 'rspec-rails'
end

gemspec
