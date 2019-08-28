# frozen_string_literal: true

source 'http://rubygems.org'

group :development do
  gem 'rubocop'
end

group :spec do
  activerecord_version =
    case ENV['RUBY_VERSION']
    when /1\.9\.3/
      3
    when /2\.1\.9/
      4
    else
      5
    end
  gem 'activerecord', "~> #{activerecord_version}"
  gem 'rspec'
  gem 'simplecov', require: false
  sqlite3_version =
    case activerecord_version
    when 3,
         4
      '1.3.6'
    when 5
      '1.4.1'
    end
  gem 'sqlite3', "~> #{sqlite3_version}"
end

group :travis do
  gem 'rake'
end
