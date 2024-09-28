---
title: Environment Variable for Google Analytics
description: Documenting my steps in adding my Google tag to my site.
date: 2024-09-26
authors: [genesis-writing]
tags:
  - blog
---

# A Learning Moment

When I originally added a Google tag to my `mkdocs.yml` file, I thought everything was fine and dandy. After reading the docs, I added the string `G-XXXXXXXXXX`, and away I went. But later, I realized I should be protecting the tag by using an environment variable. So, I removed it and forgot about it for a while.

<!-- more -->

But now we're back! The leaves are falling, the sun is setting earlier, and it's time to roast some pumpkin seeds. So I thought, hey, I should go back and add Google Analytics with an environment variable. Here we are....

## My Approach

Since I'm deploying my site using Netlify, I learned about a pretty cool feature! Turns out, you can add an environment variable directly in Netlify. So I added my key `GOOGLE_ANALYTICS_KEY` with the value (`G-XXXXXXXXXX` - my Google Analytics property ID).

I then input `!ENV GOOGLE_ANALYTICS_KEY` into `mkdocs.yml` file, commited my changes, and pushed them.

Bada bing bada boom!

## Even More New Lessons

But wait, there's more! I got an error message: `!ENV YAML`. What does this mean? My tag works correctly. I even tested it out. It turns out it could have been an extension or linter I was using.

To resolve the issue, all I did was add `!ENV` to the list of recognized tags in VS Code's YAML settings.

Ok, now I can say bada bing bada boom!

