# Capistrano::npm

npm support for Capistrano 3.x

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'capistrano', '~> 3.0.0'
gem 'capistrano-npm'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install capistrano-npm

## Usage

Require in `Capfile` to use the default task:

```ruby
require 'capistrano/npm'
```

The task will run before `deploy:updated` as part of Capistrano's default deploy,
or can be run in isolation with `cap production npm:install`

Configurable options:

```ruby
set :npm_target_path, release_path.join('subdir') # default not set
set :npm_flags, '--production --silent'           # default
set :npm_roles, :all                              # default
```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
