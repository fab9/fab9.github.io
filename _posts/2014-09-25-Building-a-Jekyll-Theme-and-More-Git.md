---
layout: post
title: "Building a Jekyll Theme"
date: 2014-09-25
author: "Fabi"
---

## Jekyll theme
Yesterday I added a theme with the automated generator. Only the main `index.html` page was showing the theme. Here's how I got the existing theme to show up on all pages.

1. In C9, inside root folder add folder called `_includes`
2. Add 2 files `_includes/head.html` and `_includes/footer.html`
3. Create another folder inside root called `_layouts`
4. New file `_layouts/post.html`
5. add this to that file:

    {% raw %}
    {% include head.html %}
      {{ content }}
    {% include footer.html %}
    {% endraw %}

6. Open main `index.html` in C9 (the one with the theme applied), copy the stuff from line 1 down to (and including) `</header>`. Lines you need to copy depend on your theme.
7. Paste into `_includes/head.html`
8. Repeat step 6 but this time copy the code at the bottom. starting at and including `<footer>` down to last line. Again, varies a little per theme.
9. Paste into `_includes/footer.html`
10. Make sure your blog post specifies which layout to use. Like this:
 
    {% highlight markdown %}
    ---  
     title: 2014-09-23-Post1
     layout: pos
    ---
    {% endhighlight %}
    
11. Forgot something... open `_includes/head.html` and modify links pointing to stylesheets and js. Example:
`<link rel="stylesheet" href="{{ root_url }}/stylesheets/styles.css">`
12. Now (still from C9) git status, add untracked files, commit, push.
13. In Github do a PR to merge feature branch into master.

That's it. :)