---
layout: post
title: "Setting up a Blog with Octopress on Heroku"
date: 2014-07-12
author: "Fabi"
---
_Update: I moved this blog from Octopress to Jekyll hosted on GitHub on Sep 2014._

##Getting Started

1. Check your `ruby --version`, it must be at least 1.9.3.

2. Download [Octopress](https://github.com/imathis/octopress), then `cd` into your blog's directory

```
$ git clone git://github.com/imathis/octopress.git test-blog
$ cd test-blog
```

3. Install dependencies

```
$ gem install bundler
$ bundle install
```

4. Install default theme

```
$ rake install
```

##Blog Configuration
I modified 4 sections of the `_config.yml`  file as shown below.

####Section 1: At the very top, contains your blog's info
```
url: http://yoursite.com #=> http://fab9.net
title: My Octopress Blog #=> fab9
subtitle: A blogging framework for hackers. #=> code wheeeeeeeee
author: Your Name #=> Fabi
simple_search: https://www.google.com/search
description:
```

####Section 2: Permalinks, Paths and More
```
root: /
permalink: /blog/:year/:month/:day/:title/ #=> /blog/:year/:month/:day
source: source
destination: public
plugins: plugins
code_dir: downloads/code
category_dir: blog/categories #=> categories
```

####Section 3: Asides
```
default_asides:
  [asides/recent_posts.html,
   asides/github.html,
   asides/delicious.html,
   asides/pinboard.html,
   asides/googleplus.html] #=>
  [asides/recent_posts.html,
   asides/github.html]
```

####Section 4: 3rd Party Settings
Pretty self-explanatory. Checkout the [docs](http://octopress.org/docs/configuring/) for more details.

---

In your `.gitignore` remove the line `public`.
Because Octopress compiles its generated content, i.e. static version of your site, into the `public` directory, we need to make sure everything in this dir is included in our git repo.

##Get Ready to Write!
```
$ rake new_post["title"] # Creates post
```
```
$ rake generate # Generates the post into public/source/_posts
$ rake preview # Go to http://localhost:4000/ on your browser to preview.
```

Open up the generated file in a text editor. At the very top is a block of yaml code where you can change a few things.

At first it looks sort of like this:

```
---
layout: post
title: "First post"
date: 2014-07-12 11:03:38 -0400
comments: true
categories:
---
```

Here you can do a few things. For example:

- When working on a draft add `published: false`.
- Add one category  `categories: heroku`, or many: `categories: [heroku, git, octopress]`

##Octopress + Heroku

```
$ gem install heroku
$ heroku login
```

###Pointing your custom domain to Heroku
Check out the docs at [Heroku](http://devcenter.heroku.com/articles/custom-domains).
Set your root domain, your-domain.com, to redirect to www.your domain.com.

Confirm that your DNS is configured correctly with the `host` command:
```
$ host www.example.com // www.example.com is an alias for example.herokuapp.com
```

##Deploy
```
 $ git push heroku master
```

####Further Reading

 - [Octopress Documentation](http://octopress.org/docs/)
 - http://www.jackiejohnston.us/blog/setting-up-an-octopress-blog-on-heroku/

