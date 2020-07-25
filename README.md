![Build and deploy Jekyll site to GitHub Pages](https://github.com/Porkbutts/finance.adriant.io/workflows/Build%20and%20deploy%20Jekyll%20site%20to%20GitHub%20Pages/badge.svg)

# finance.adriant.io

<https://finance.adriant.io> is my personal finance blog built using Jekyll and hosted on Github-pages.

## Installation
- You must have **ruby** installed. **rvm** or some kind of Ruby version manager is recommended.
- You must have **bundler2**. You can install with
```
$ gem install bundler
```
- Install the gems from Gemfile using `bundle` command.


## Run locally
```
# Run dev environment with drafts, livereload and without analytics, comments, ads
$ script/serve-dev

# Run a production build
$ script/serve-prod
```

### Known Issues
Seems like `livereload` doesn't work on Windows and I already tried the suggestion from [this blog](https://httpain.com/blog/jekyll-live-reload-windows/). So just disable it for now.

## Deployment
Commits to the `master` branch will automatically trigger CI/CD defined in the [Github Actions](./.github/workflows/github-pages.yml). This will collect tags, build the jekyll site and commit the static site to the `gh-pages` branch.

## Contributing

### Drafting Posts
Add to `_drafts` with the file name format `YYYY-mm-dd-name-of-post.md`

Here's an example post. It should include the category, comma-delimitted tags,
and optionally a read more separator.
```
---
layout: post
categories: aws kubernetes
tags: s3 eks
---

Hello I'm here to talk about s3 and eks.

<!--more-->

<Users only see this content when they click into the blog post>.
```

When the post is ready to be published, move it to `_posts`.

### \_includes helpers

#### image.html
Use this to embed an image.
```
{% include image.html file=FILE[, alt=ALT, width=WIDTH, height=HEIGHT] %}
```

### Adding new gems
```
$ bundle add <gem>
```

If it is a jekyll plugin, you may need to add it to the `plugins` section in `_config.yml`

## Gotchas
Not all jekyll plugins are supported by Github pages. I guess it makes sense, they don't read the Gemfile and install your deps, they just have a preset environment. Here's a list of supported plugins: https://pages.github.com/versions/

## Useful Reading
- [Jekyll permalinks](https://jekyllrb.com/docs/permalinks/)
- [Jekyll github-pages](https://jekyllrb.com/docs/github-pages/)
- [Jekyll site variables](https://jekyllrb.com/docs/variables/)
- [Jekyll blogging](https://jekyllrb.com/docs/step-by-step/08-blogging/)
