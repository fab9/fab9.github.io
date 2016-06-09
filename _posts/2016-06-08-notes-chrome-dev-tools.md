---
layout: post
title: "Chrome DevTools Part 1"
date: 2016-06-08
author: "Fabi"
---

Chrome's DevTools are awesome, I use certain features everyday but others are a mystery to me. It's time to learn new tricks, and what better way than watching  'Frontend Masters' (looove them), '[Mastering Chrome DevTools](http://livestream.com/accounts/4894689/events/5453917)' workshop. 

The instructor, [Jon Kuperman](https://github.com/jkup) divided  his material into 3 parts: Editing, Debugging and Profiling, which span 6 videos total.

Here's my notes from video #1:

---

# Editing
**Device emulation** mode is NOT perfect but it gets you pretty far. When you pick a device like an iPhone 6, it's not just changing the viewport size, it's actually changing the *headers* your site throws so you can get a pretty close experience. Responsive design mode just throws a web header.

**Workspaces**  
Fantastic feature _if_ your project doesn't have a complicated build process. Workspaces is able to persist changes by mapping  resources served from a local web server to files on a disk, so while it works beautifully when mapping `.css` => `.css` files for ex,  Sass and LESS are not supported. Chrome is adding support for Sass pre-processing but it's not released yet.

If you're doing JavaScript transpiling with Babel, there's no support for that either.