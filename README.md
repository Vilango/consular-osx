# Consular - OSX Core

Automate your OSX Terminal with Consular


# Setup && Installation

If you haven't already, install Consular:

    $ gem install consular

then install consular-osx:

    $ gem install consular-osx


next, run `init`:

    $ consular init

This will generate a global directory and also a `.consularc` in your home
directory. On the top of your `.consularc`, just require this core like
so:

```ruby
# You can require your additional core gems here.
require 'consular/osx'

# You can set specific Consular configurations
# here.
Consular.configure do |c|
end
```

Now you can use OSX Terminal to run your Consular scripts!


# Here are some OSX Terminal specific samples for your .term DSL files

window "console", :bounds => [0, 451, 1680, 900], :miniaturized => true do 
  run " cd \"#{project_dir}\""
  run " rails c"
end



# local building

gem build consular-osx.gemspec && gem install consular-osx --no-rdoc --no-ri && consular start odm


