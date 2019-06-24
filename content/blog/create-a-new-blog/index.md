---
title: "Create a Blog in 10 Minutes"
date: "2019-05-12"
description: "How to set up a blog using Gatbsby and Netlify."
---

## Hello Gatsby, Netflify and World

I've been a Developer for over a decade but I've never really done the blogging thing. In the spirit of adventure, I've decided to give it a try, so here's a post about how to set up a blog if you own a domain, have a modicum of technical ability and roughly 10 minutes to spare.


## Executive Summary - tldr;

Install Gatsby -> Write post(s) ->  Push to Github -> Deploy to Netlify

## Hang On, What?

Ok, that was a little brief. Here's a slightly longer version:

1. Blogs are a surprisingly time-consuming thing to set up, despite the fact that it's (already half-way through!) 2019. Unless you're happy with Medium, of course.

2. [Gatsby](https://www.gatsbyjs.org/) is a 'free and open source framework based on React that helps developers build blazing fast websites and apps'. It's pretty fly, and has some very useful [tutorials](https://www.gatsbyjs.org/tutorial/) if you need them. For blogs, there's a [starter repo](https://github.com/gatsbyjs/gatsby-starter-blog) - this is what we'll be using. 

3. Don't worry if you don't know React or are rusty or whatever, you can get up and running with literally no Javascript know-how. If you already know some Markdown it's a bonus but it's easy to pick up.

4. You will need to have installed [Node](https://nodejs.org/) and know how to use npm via the command line, as well as be familiar Git... a bit. However, it makes no difference if it's -hub, -lab or -bucket.

5. When it comes to publishing to the Actual World, [Netlify](https://www.netlify.com/) is your friend. As in, you point Netlify at your repo, configure your DNS and that's pretty much it.

## How To - Step by Step

Let's get to it. Open up your Command Line tool of choice and install Gatsby:

```
npm install -g gatsby-cli
```

(the `-g` flag installs a package globally so it can be called from the command line)

After it finishes, you can create your first blog with the command `gatsby new`, providing a name for your new blog and a link to the starter project `gatsby-starter-blog` that will be cloned into your working directory (there are lots of starters available, see [https://www.gatsbyjs.org/starters/?v=2](here)).


```
gatsby new my-new-blog https://github.com/gatsbyjs/gatsby-starter-blog
```

Assuming npm did its magic without any hitches, you should now be able to `cd` in to your new blog and start it up:

```
cd my-new-blog
gatsby develop

```


Boom! Your blog is alive. If you look at the console output you should see:

```
You can now view gatsby-starter-blog in the browser.

http://localhost:8000/

```

Visit that link in a browser and you should see the Gatsby starter blog page - boom!

At this point you can spend time poking/hacking about in the project to update the bio and add your first post, but I'm going to leave that side of things up to the reader for now and move on to publishing.


## Push to Github

First, head to Github and [create a new repo](https://github.com/new) without ticking the 'Initialize this repository with a README' checkbox. Then return to your terminal to intialise your repo, add files if necessary and commit them:

```
\\ in your project root directory
git init
git add .
git commit -m "Initial commit"
```

Then push to Github:
```
git remote add origin https://github.com/[your-name-here]/[your-repo-name-here].git
git push -u origin master
```

Assuming that went smoothly, you can now refresh the Github repo page and see your project has been pushed.


## Publish via Netflify

This is perhaps the easiest deploy you'll ever do.

1. Visit [Netlify](https://www.netlify.com/) and sign in or create a free account if you don't have one already.
2. Select 'New site from Git'.
3. Choose your Git provider and then sign in to grant Netlify access.
4. You should now see your new blog in the list of repos. Select it.
5. Assuming you haven't made any changes to the default set-up, you can skip the deploy settings page and go straight to 'Deploy site'
6. Gatsby will now create a deployment pipeline for you, and after a short time your new blog will be published to an auto-generated url.
7. It's alive!

The only remaining steps are to set up your domain and optionally add SSL using the Netlify tools, which are frankly amazing.

In the next post I'll go into some of the Gatsby customisations and configs that I've picked up. In the mean time, happy blogging!
