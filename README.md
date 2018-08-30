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

```txt
---
layout: default
img: code.png
title: The section title
---
The description of this section
```

## Demo
View this jekyll theme in action [here](https://swcool.github.io/landing-page-theme)
For more Jekyll details, read [documentation](http://jekyllrb.com/).

## License
The contents of this repository are licensed under the [Apache 2.0](http://www.apache.org/licenses/LICENSE-2.0.html).

## Version
1.0.1
