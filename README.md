# BFM public website 

The website uses github pages through the [Jekyll](https://jekyllrb.com/) static site generator and its implemtation is based on the Landing Page theme [landing-page bootstrap theme ](http://startbootstrap.com/templates/landing-page/)

## Visualize the current website

https://cmcc-foundation.github.io/www.bfm-community.eu/

## Develop locally

 - Install jekyll and bundler from
   [RubyGems](https://rubygems.org/pages/download) as described in the
   Jekyll [Quick-start guide](https://jekyllrb.com/docs/quickstart/);
 - Clone this repo;
 - download dependencies with bundler:
   ```shell
   bundle install
   ```
 - run the site locally and start editing content:
   ```shell
   bundle exec jekyll liveserve
   ```

## How to use

### Add a section to the Homepage

 - Place a image in `/img/services/`
 - Create posts to display your section in the homepage. Use the
   following as an example:

```yaml
---
layout: default
img: code.png
title: The section title
---
The description of this section
```

### Add a secondary page

Create a Markdown page in the project root with a "page" layout, a
title and an id. For example, this is the Jekyll front matter for the
[BFM Quick guide](bfm-quick-guide.md):

```yaml
---
layout: page
title: Quick Guide
id: quick-guide
description: |
---
```

### Change the header, footer, about or contact sections in the Home page

Go to the Jekyll partials directory in [_includes](_includes) and find
out the section you want to modify.

For example, if you want to change the "about" text, [edit the
about.html file](_includes/about.html) directly in the Github editor,
or in your local working directory.

### Website SEO Optimization

Please follow [this guide](https://help.github.com/articles/search-engine-optimization-for-github-pages/).

## Demo
View this jekyll theme in action [here](https://swcool.github.io/landing-page-theme)
For more Jekyll details, read [documentation](http://jekyllrb.com/).

## License
The contents of this repository are licensed under the [Apache 2.0](http://www.apache.org/licenses/LICENSE-2.0.html).

## Version
1.0.1
