1. Hashes don't require curly braces when they are the last argument called on a function
2. Symbols containing dashes require hash rockets instead of colons
3. Steps to add Bootstrap:

  1. Add `gem 'bootstrap-sass', '2.3.2.0'` and `gem 'sprockets', '2.11.0'` to the Gemfile
  2. `bundle install`
  3. Restart server if already running
  4. Add `config.assets.precompile += %w(*.png *.jpg *.jpeg *.gif)` to make bootstrap-sass compatible with the asset pipeline
  5. Create `custom.css.scss` under `app/assets/stylesheets/`
  6. Add `@import "bootstrap";` to `custom.css.scss`

4. Three principal features of the asset pipeline:

  1. Asset directories

    * app/assets: assets specific to the present application
    * lib/assets: assets for libraries written by your dev team
    * vendor/assets: assets from third-party vendors

  2. Manifest files - you can use manifest files to tell Rails (via the Sprockets gem) how to combine them to form single files

  3. Preprocessor engines - specified by filename extensions (ie: scss for Sass, .coffee for CoffeeScript(see [RailsCast on CoffeeScript basics ](http://railscasts.com/episodes/267-coffeescript-basics) for a good place to start), and .erb for embedded Ruby (ERb))

5. Rails routes - [A good read on rails routes](http://guides.rubyonrails.org/routing.html)

6. Generate integration test: `rails g integration_test user_pages` will create user_pages_spec.rb

7. Generate user's controller `rails generate controller Users new --no-test-framework`. In this case `new` is the action automatically generated in the `Users` controller because we specified it. This also creates a `users/new.html.erb` under 'app/views'
