# barebones-jekyll

A barebones website template for students to fork while learning how to build a GitHub website. 


## Will teach you how to use themes like these:

* [contrast](https://github.com/niklasbuschmann/contrast)
* [polar bear theme] (https://github.com/diezcami/polar-bear-theme)
* [lanyon](http://lanyon.getpoole.com/)

# your minimal site:

```
site  
├── index.md   
├── config.yml  
├── assets folder  
│   └── images    
│   └── CSS files  
├── _layouts folder  
│   └── default.html  
│   └── page.html   
└── _includes folder   
    ├── head.html  
    ├── header.html  
    ├── navbar.html  
    └── footer.html  
``` 
  
## index.md

Landing page. 


## config file

Basic example from [GitLab](https://gitlab.com/pages/jekyll/blob/master/_config.yml):

````
# Welcome to Jekyll!
#
# This config file is meant for settings that affect your whole blog, values
# which you are expected to set up once and rarely edit after that. If you find
# yourself editing this file very often, consider using Jekyll's data files
# feature for the data you need to update frequently.
#
# For technical reasons, this file is *NOT* reloaded automatically when you use
# 'bundle exec jekyll serve'. If you change this file, please restart the server process.
#
# If you need help with YAML syntax, here are some quick references for you: 
# https://learn-the-web.algonquindesign.ca/topics/markdown-yaml-cheat-sheet/#yaml
# https://learnxinyminutes.com/docs/yaml/
#
# Site settings
# These are used to personalize your new site. If you look in the HTML files,
# you will see them accessed via {{ site.title }}, {{ site.email }}, and so on.
# You can create any custom variable you would like, and they will be accessible
# in the templates via {{ site.myvariable }}.

title: Example Jekyll site using GitLab Pages
email: your-email@domain.com
description: >- # this means to ignore newlines until "baseurl:"
  Write an awesome description for your new site here. You can edit this
  line in _config.yml. It will appear in your document head meta (for
  Google search results) and in your feed.xml site description.
baseurl: "/jekyll" # the subpath of your site, e.g. /blog
url: "/" # the base hostname & protocol for your site, e.g. http://example.com
twitter_username: jekyllrb
github_username:  jekyll
gitlab_username:  pages

# Build settings
theme: minima
plugins:
  - jekyll-feed

# Exclude from processing.
# The following items will not be processed, by default.
# Any item listed under the `exclude:` key here will be automatically added to
# the internal "default list".
#
# Excluded items can be processed by explicitly listing the directories or
# their entries' file path in the `include:` list.
#
# exclude:
#   - .sass-cache/
#   - .jekyll-cache/
#   - gemfiles/
#   - Gemfile
#   - Gemfile.lock
#   - node_modules/
#   - vendor/bundle/
#   - vendor/cache/
#   - vendor/gems/
#   - vendor/ruby/

````
  
Longer example: https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml
