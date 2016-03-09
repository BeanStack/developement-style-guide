# Beanstack Development Guidelines

This document provides a set of recommended guidelines when it comes to developing web applications using Rails as its core. While guideline create strict constraints, its helps reduce development debt and promote a culture of good development habits and standards.


## Pre-development Readings

**Coding style guide**
https://github.com/bbatsov/rails-style-guide
https://github.com/bbatsov/ruby-style-guide
http://isobar-idev.github.io/code-standards/
https://github.com/airbnb/javascript/tree/master/react

**CSS style guide**
https://smacss.com/

**Videos**
https://www.youtube.com/playlist?list=PLuVcDOUVjW2ePvFapFSHBZ71ya2fLHZS5

**Git Workflow**
https://guides.github.com/introduction/flow/index.html


## Basic Environment

1. Postgres App
2. Homebrew
3. RVM
4. Command Line Tools

## Production & Staging Environment

1. Passenger & Nginx
2. Sidekiq
3. Redis-server

## Editing Softwares

**Development Tools**
1. Sublime Text
2. Github Desktop

**External Debugging**
1. RailsPanel Chrome Extension


## Starting a new Project

```
# Create a new rails project with Postgre as its database
$rails new app_name -T -d=postgresql
```

**Initial Configuration**
```
config.time_zone = 'Singapore'

# Only for active_record
config.active_record.default_timezone = :local

# Configure sensitive parameters which will be filtered from the log file.
config.filter_parameters += [:password]

# Configure default generators
config.generators do |g|
  g.helper false
  g.stylesheets false
  g.javascripts false
end
```

## Preparing for Production

Code Analysis
1. Sentry, Code Climate and Circle CI

Website Checker
1. Pingdom for uptime monitoring
2. New Relic for performance tracking
