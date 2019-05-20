---
title: "Create a Blog in 10 Minutes"
date: "2019-05-12"
description: "How to set up a blog using Gatbsby and Netlify."
---

# Hello Gatsby, Netflify and World

I've been a Developer for over a decade but I've never really done the blogging thing. In the spirit of adventure, I've decided to give it a try, so here's a post about how to set up a blog (quite meta :wink:) if you have a domain, a modicum of technical ability and about 10 minutes to spare.


## Executive Summary - tldr;

Install Gatsby -> Write post(s) ->  Push to Github -> Deploy to Netlify

## Hang On, What?

Ok, that was a little brief. Here's a slightly longer version:

1. Blogs are a surprisingly time-consuming thing to set up, despite the fact that it's (already half-way through!) 2019. Unless you're happy with Medium, of course.

2. [Gatsby](https://www.gatsbyjs.org/) is a 'free and open source framework based on React that helps developers build blazing fast websites and apps'. It's pretty fly, and has some very useful [tutorials](https://www.gatsbyjs.org/tutorial/) if you need them. For blogs, there's a [starter repo](https://github.com/gatsbyjs/gatsby-starter-blog) - this is what we'll be using. 

3. Don't worry if you don't know React or are rusty or whatever, you can get up and running with literally no Javascript know-how. If you already know some Markdown it's a bonus but it's easy to pick up.

4. You will need to have installed [Node](https://nodejs.org/) and know how to use npm via the command line, as well as be familiar Git... a bit. However, it makes no difference if it's -hub, -lab or -bucket.

5. When it comes to publishing to the Actual World, [https://www.netlify.com/](Netlify) is your friend. As in, you point Netlify at your repo, configure your DNS and that's pretty much it!

## How To - Step by Step

Let's get to it. Open up your Command Line tool of choice and install Gatsby:

```
npm install -g gatsby-cli
```

(the `-g` flag installs a package globally so it can be called from the command line)

After it finishes, you can create your first blog with the command `gatsby new`, providing a name for your new blog and a link to the starter project `gatsby-starter-blog` (there are lots of starters available, see [https://www.gatsbyjs.org/starters/?v=2](here)), 

```
gatsby new my-new-blog https://github.com/gatsbyjs/gatsby-starter-blog
```

Assuming npm did its magic without any hitches, you should now be able to cd in to your new blog and start it up:

```
cd my-new-blog
gatsby develop

```