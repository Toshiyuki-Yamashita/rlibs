# frozen_string_literal: true

require "bundler/gem_tasks"
require "rspec/core/rake_task"

RSpec::Core::RakeTask.new(:spec)

require "rubocop/rake_task"

RuboCop::RakeTask.new

task default: %i[spec rubocop]

task push: :build do |_t|
  sh "gem push --key github --host https://rubygems.pkg.github.com/Toshiyuki-Yamashita pkg/lib_july-#{July::VERSION}.gem"
end
