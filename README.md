# Heroku buildpack: No!

This is a [Heroku buildpack][buildpack] for failing builds.

If you're using pipelines (and you should!), you might want to enforce that
you only promote to your production environment. This buildpack prevents you
from accidentally deploying to production manually by failing any build
attempt.

[buildpack]: https://devcenter.heroku.com/articles/buildpacks
    "Heroku Dev Center article on buildpacks"


## Usage

Run the following commands to overwrite existing buildpacks:

    $ heroku buildpacks:clear
    $ heroku buildpacks:set heroku-community/no
