# Rails-AdminLTE-Bower-Boilerplate (RABB)

## Requirements

* Bower

## Installation

`bundle install`
`bower install`

## Run

### Development

To use `foreman`, just copy `Procfile.dist` to `Procfile` and run `foreman start`

### Production

// TODO

## Details

Instead of trying to have Rails manage my frontend dependencies, I only use the Rails Assets Pipeline for the JS libs
that have to be gems because they interact in some way with the server: jQuery + turbolinks, cocoon, etc...

While all other JS and CSS dependencies (Bootstrap, Font-awesome, etc...) are managed with Bower which is much better at this job.

Bower install all its dependencies in `vendor/assets/bower_components` and Rails knows where to find them thanks to this line in `config/initializers/assets.rb`:

```
Rails.application.config.assets.paths << Rails.root.join('vendor', 'assets', 'bower_components')
```

