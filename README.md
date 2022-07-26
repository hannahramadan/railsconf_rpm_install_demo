# README

This is a simple Rails app for the purpose of demonstrating how to install the New Relic Ruby agent. The latest released gem for the Ruby agent can be found at [Rubygems.org](https://rubygems.org/gems/newrelic_rpm)

## Install Instructions

### Create a New Relic account
Create a free [New Relic account](https://newrelic.com/signup). Or [sign in](https://one.newrelic.com/)


### Install the gem
The Ruby agent's gem is available from rubygems.org as newrelic_rpm. For applications using Bundler, add this gem to the Gemfile:
gem 'newrelic_rpm'

```ruby
gem 'newrelic_rpm'
```

and run `bundle install` to activate the new gem.

If you're using Rails 3 or higher, or Rails 2.3 in the [recommended configuration](https://bundler.io/v1.12/rails3.html), Rails will automatically call `Bundler.require` and cause `newrelic_rpm` to be required during startup of your application.


### Install the configuration file
After installing the agent, you will need to install the `newrelic.yml` configuration file and name your app. 

Generate a `newrelic.yml` file with the following command:

```ruby
newrelic install --license_key="YOUR_KEY" "My application"
```

You can find your New Relic License Key under your Account -> API Keys.


## Uninstall Instructions
To uninstall the Ruby agent using Bundler, remove `gem 'newrelic_rpm'` from your Gemfile.
