# Template Repository
In order to use this project as a template repo, you should update a few things.

## `_config.yml`
This file should contain most of the application config settings that need to be updated, such as site name, description, google analytics code, etc.

## `CNAME`
This file contains the domain you want to use for your Github Pages website.

## Github Pages access token
Create a Github personal access token with `public_repo` access. Then create a secret environment on your Github repo named `JEKYLL_PAT`. This is referenced in the [Github Actions](./.github/workflows/github-pages.yml).

## `README.md`
Obviously this will be specific to your site. You can fetch the build status badge from Github Actions after the first run.
