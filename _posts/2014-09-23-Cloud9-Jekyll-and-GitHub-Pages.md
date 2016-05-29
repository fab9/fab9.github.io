---
layout: post
title: "Cloud9, Jekyll and GitHub Pages"
date: 2014-09-23
author: "Fabi"
---

## Misc notes

### Cloud9
an IDE, connects to your github acct

### Jekyll
http://jekyllrb.com/docs/home/


In Cloud9 `cramdown` is the markdown gem.  
`gem install jekyll`

To serve locally (using Terminal) it would be `jekyll serve` but in C9 you do: `jekyll build` > _Run with... Apache httpd (PHP, HTML)_ > visit your site with the link it gives you.

Jekyll reads the markdown files and translates them to html files and wraps them in  a nice template as well so you get something pretty. Github does this automatically. Github automatically runs Jekyll against your repo whenever you push into master github will turn files into website.

Any changes you make to the html that it generates, you'll see those changes reflected immediately.

#### Further reading
- http://code.tutsplus.com/articles/building-static-sites-with-jekyll--net-22211

#### Examples of `config.yaml` files
- https://github.com/maciakl/Sample-Jekyll-Site/blob/master/_config.yml
- http://learn.andrewmunsell.com/learn/jekyll-by-example/tutorial

#### Git Clones and Forks
- http://stackoverflow.com/questions/6286571/git-fork-is-git-clone
- http://stackoverflow.com/questions/3903817/pull-new-updates-from-original-github-repository-into-forked-github-repository?lq=1

---
A merge commit has 2 parents. I represent a commit that tells you where these 2 (merged branches) came from(?)

Merge commits are not super handy most of the time. github doesn't show them must of the time but they are in there, these merge commits exist.

---

**Rebasing** is for getting other peoples' work onto mine.

---

[Semantic Versioning](http://semver.org/)

