Ruby on rails tutorial: sample application

This is the sample application for ruby on rails tutorial
sample_app

NOTE:
=====
This code is fully working sample from Ruby on rails tutorial chapter 3. The book self didn't tell you the following things which were quite important for the beginner like me. I had spent at least 4 hours to complete this chapter demo. To save you time, whenever you get stuck in this chapter, check the following items

* Receive "undefined method `visit' for ..." error, you may need to add the "config.include Capybara::DSL" in the spec_helper.rb class (see: https://github.com/rspec/rspec-rails/issues/503)

* Receive "`require': cannot load such file -- nokogiri" error, to fix this, you need to run "bundle update capybara" twice, it will then install the nokogiri.

* In 3.3 dynamic pages section, if you need to check your gem files to make sure 'capybara' used 1.1.2 version e.g. gem 'capybara', '1.1.2', if you didn't specify the version, it will use 2.1 version which has a big change.

# Eliminating bundle exec
1. Run the following script
'''bash
$ rvm get head && rvm reload
$ chmod +x $rvm path/hooks/after cd bundler
$ cd  ̃/rails projects/sample app
$ bundle install --without production --binstubs=./bundler_stubs

2. Add "bundler_stubs/" into .gitignore
3. If add another command, you need to run "$ bundle install --binstubs=./bundler_stubs
" again.

