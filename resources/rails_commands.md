## RAILS COMMANDS



### Working with RSpec Testing Framework

#### Installation

Once you have already added rspec's gem into the `Gemfile`, run the following commands.

Installing the gem
```console
  $ bundle install
```

Generating configuration files
```console
  $ rails generate rspec:install
```

Running the above command, it should created these files.
```console
      create  .rspec
      create  spec
      create  spec/spec_helper.rb
      create  spec/rails_helper.rb
```

Now when you generate a model or controller, instead of creating necessary files of tests, it will create those files for you.
_Example:_
```console
  $ rails generate controller tests hola hola2
```

```console
    create  app/controllers/tests_controller.rb
    route  get 'tests/hola'
           get 'tests/hola2'
    invoke  rspec
    create    spec/requests/tests_spec.rb
```

**Running our specs**.      

Default: Run all spec files (i.e., those matching spec/**/*_spec.rb)
```console
  $ bundle exec rspec
```


Run all spec files in a single directory (recursively)
```console
  $ bundle exec rspec spec/models
```


Run a single spec file
```console
  $ bundle exec rspec spec/controllers/accounts_controller_spec.rb
```

Run a single example from a spec file (by line number)
```console
  $ bundle exec rspec spec/controllers/accounts_controller_spec.rb:8
```

See all options for running specs
```console
  $ bundle exec rspec --help
```
