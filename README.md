# Osiris Theme for Hugo

Osiris is a simple minimalist theme for [Hugo blog engine](https://gohugo.io/).

![Osiris Screenshot](https://raw.githubusercontent.com/sudarshan-reddy/hugo-theme-anubis/master/images/screenshot.png)

## Features

- Pagination
- Tags/Categories support
- Archive
- Mobile support
- Google Analytics
- Disqus
- RSS feeds
- Translations (en, ru, fr, pl)
- Multilingual mode 
- Robots.txt 
- Favorite posts

## Installation

Inside the folder of your Hugo site run:

    $ git submodule add https://github.com/sudarshan-reddy/hugo-theme-osiris.git themes/osiris

For more information read the official [setup guide](//gohugo.io/overview/installing/) of Hugo.

## Getting started
After installing the theme successfully it requires a just a few more steps to get your site running.

### Update config file

Example of config.toml:
```toml
baseURL = "https://baseurl.com"
languageCode = "en-us"
title = "Your Blog"
theme = "osiris"
paginate = 5

disqusShortname = ""
googleAnalytics = ""

[author]
  name = "Sudarshan"

[params]
   author = "Sudarshan Reddy"

[menu]

  [[menu.main]]
    identifier = "about"
    name = "About"
    url = "/about/"
    weight = 1

  [[menu.main]]
    identifier = "tags"
    name = "Tags"
    url = "/tags/"
    weight = 2

  [[menu.main]]
    identifier = "github"
    name = "Github"
    url = "https://github.com/sudarshan-reddy/"
    weight = 3

[taxonomies]
category = "categories"
tag = "tags"
```

### Check your site

In order to see your site in action, run Hugo's built-in local server.

`$ hugo server`

Now enter [`localhost:1313`](http://localhost:1313/) in the address bar of your browser.

## Feature Settings

### Google Analytics
Only works for production environment. You either build your site with variable like
`HUGO_ENV=production hugo --minify`
or just put `env: production` to `params` section of config.

### Robots.txt
Based on environment.  
For production — allow all, for other — disallow all.

### Favorite posts
To mark posts as favorite just add `favorite: true` in post's front matter. It adds a "★" icon nearby post's title. 

## License
MIT

(c) Sudarshan Reddy
2020
