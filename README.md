# ECS Bundler 
[![Gem Version](https://badge.fury.io/rb/ecs_bundler.svg)](https://badge.fury.io/rb/ecs_bundler)

Composer module to transfer dependency information to our ECS server. Find the solution at https://ecs-app.eacg.de

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'ecs_bundler'
```

And then execute:
```
$ bundle
```

Or install it yourself as:
```
$ gem install my_gem
```

To store your credentials for automated transfer you may create `.ecsrc.json` in your project directory or in your home directory to set credentials globally (not recommended!)

`.ecsrc.json` example:

```json
{
  "userName": "UserName",
  "apiKey": "apiKey",
  "url": "url",
  "project": "Project Description"
}

```

## Usage

You also may initiate transfer to ECS server manually by executing following command via terminal:
 
```
ecs_bundler
ecs_bundler -u userName -k apiKey -p Project 
ecs_bundler -c config.json
```
```
Usage: ecs_bundler [switches|options]
Switches:
   --help (-h) - display this help message
   --version - display version string
Options:
   --apiKey (-k) - api key
   --userName (-u) - user name
   --url - Base url
   --project (-p) - Project name
   --config (-c) - Config path
```
You also may initiate transfer to ECS server manually by executing following command in rake task or any other place:
```ruby
ECSBundler.run
```
