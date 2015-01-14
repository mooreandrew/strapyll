Strapyll
===================
[![Build Status](https://travis-ci.org/MashSoftware/strapyll.svg?branch=master)](https://travis-ci.org/MashSoftware/strapyll)

Strapyll is a HTML toolkit that brings together some of the most popular and easy to use website templating, generation, styling, testing, deployment and hosting components.

The aim is to allow you to focus on the most important thing; your content.

Made with [Jekyll](http://jekyllrb.com/), [Bootstrap](http://getbootstrap.com/), [Bootswatch](http://bootswatch.com/) & [Font Awesome](http://fortawesome.github.io/Font-Awesome/).

Tested with [HTML Proofer](https://github.com/gjtorikian/html-proofer).

Deployed by [Travis CI](https://travis-ci.org/).

### Prerequisites
* [Ruby](https://www.ruby-lang.org/en/downloads/)
* [RubyGems](http://rubygems.org/pages/download)
* [Bundler](http://bundler.io/)

## Getting started
```
git clone git@github.com:MashSoftware/strapyll.git
cd strapyll
bundle install
bundle exec jekyll serve
```
Go to [http://0.0.0.0:4000/](http://0.0.0.0:4000/)

### Adding pages
Place a new HTML file in the root directory and add following Front Matter YAML:
```
---
layout: navbar_footer
title: My New Page
permalink: /my-new-page/
---
```
Then go to [http://0.0.0.0:4000/my-new-page/](http://0.0.0.0:4000/my-new-page/) to see the new blank page and start focussing on your content.

### Running tests
This is the same script that Travis runs during the build, run this locally before pushing to avoid broken builds:
```
./script/cibuild
```

### Deploying with Travis
```
travis enable
git commit -a -m "super awesome commit message"
git push
```

## Next steps
### Changing themes
Change the ```theme``` setting in ```_config.yml``` to any of the [Bootswatch](http://bootswatch.com/) theme names and restart the server.


### Changing layouts
There are two basic layouts included with Strapyll:
 * ```navbar_footer``` - a fixed navbar with a sticky footer.
 * ```navbar_sidebar``` - a fixed navbar with a sidebar.

Include either in your Front Matter ```layout``` element to use them.

Go to [http://0.0.0.0:4000/navbar-footer/](http://0.0.0.0:4000/navbar-footer/) or [http://0.0.0.0:4000/navbar-sidebar/](http://0.0.0.0:4000/navbar-sidebar/) to preview them.


### Making new layouts
The ```_includes``` directory contains all the partial HTML needed to construct a new layout.

Place your ```{% include <example>.html %}``` tags within your templated HTML in the ```_layouts``` directory. The ```{% include head.html %}``` and ```{% include scripts.html %}``` includes are required to use Bootstrap, Bootswatch and Font Awesome, or replace them with your own.

### Everything else
Please refer to the documentation for the various components used:
 * [Jekyll](http://jekyllrb.com/docs/home/)
 * [Bootstrap CSS](http://getbootstrap.com/css/)
 * [Bootstrap Components](http://getbootstrap.com/components/)
 * [Bootstrap Javascript](http://getbootstrap.com/javascript/)
 * [Font Awesome Icons](http://fortawesome.github.io/Font-Awesome/icons/)
 * [Font Awesome Examples](http://fortawesome.github.io/Font-Awesome/examples/)
 * [HTML Proofer](https://github.com/gjtorikian/html-proofer)
 * [Travis CI](http://docs.travis-ci.com/)
