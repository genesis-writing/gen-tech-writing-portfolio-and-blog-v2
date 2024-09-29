---
title: YAML and Python
description: Sharing key lessons I learned about YAML and Python
date: 2024-07-08
authors: [genesis-writing]
tags:
  - blog
---

# Important Lessons

Today, I learned how finnicky YAML is when it comes to indentations. One wrong move and nothing works. It turns out I needed to change my indentation levels to get various plugins to work on my site.

<!-- more -->

I also learned that I need to update my `requirements.txt` file whenever I add new dependencies. This was the reason my Netlify builds failed earlier today. I'll remember this for next time! If you're wondering what a `requirements.txt` file is, check out <u>[**this article**](https://www.freecodecamp.org/news/python-requirementstxt-explained/)</u> by **Tantoluwa Heritage Alabi** at freeCodeCamp!

Oh yeah, here's the command that I didn't run before my build to update my file:

```bash
pip3 freeze > requirements.txt
```