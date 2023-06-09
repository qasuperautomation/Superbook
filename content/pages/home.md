---
title: QA Guidance
date: Last Modified
permalink: /
eleventyNavigation:
  key: QA Guidance
  title: QA Guidance
  order: 0
---
This QA Guidance is a documentation of testing which guarantees that the user receives a high-quality product with minimal bugs and maximum amount of time to assure each release is the highest quality of Dashboard and Apps for Aplikasi Super. 

**To Evaluate** 🔍 quality of an application and also for improving it, by identifying defect and problem of system failure as early as possible.

**Reability** 💪 **:** aimed zero bugs when release to production

**Usability** 💎 **:** targeting smooth experience when customer use our product

\
If you click that button and follow the steps, the Netlify robots will copy the spacebook repository to your own personal Github account. Once complete, your new spacebook will be automatically deployed to the cloud with its own URL and ready for customization. 👍

- - -

::: callout-blue
**Did you know?** You can host your project anywhere, but we currently assume [Netlify](https://www.netlify.com/), and various features may be Netlify dependent (e.g. contact forms, Netlify Identity).  They provide a generous free tier, and are pioneers in a new breed of web hosting that makes it simple to push some files to a speedy, global CDN that will serve your files faster than you can blink.
:::

- - -

## What is a spacebook?

A spacebook is a simple website generator that will help you create your own project just like this one using a bunch of cool, modern, and fast technology:

* [Eleventy](https://www.11ty.io) a super fast Node-based static site generator that stays out of your way and lets you ship only what you want to ship 🚀
* [Tailwind 2.0](https://tailwindcss.com/) a brilliant and tiny utility-first CSS framework 🎨
* [Alpine.js](https://github.com/alpinejs/alpine) a minimal utility-first framework for simple or advanced JavaScript 🕹️
* [Elasticlunr](http://elasticlunr.com/) a lightweight full-text search engine 🔍
* [Advanced Markdown-it support](https://github.com/markdown-it/markdown-it) with footnotes, custom containers, emoji support, tables, task lists, and auto-linked images ✏️
* [Netlify CMS](https://www.netlify.com/) *(optional)* to provide an easy Markdown editor for creating and changing content. 💻

Never fear! You don't need to know or understand any of this to launch a spacebook, but it results in a speedy, easy-to-use, and accessible website that typically scores 100s across the board on Google Lighthouse metrics for mobile and desktop.

::: callout
**Did you know?** If you wish, you may customize the design of your spacebook, or even use it as the basis for your creating your own starter. It was built on the [shoulders of giants](/credits). 👍
:::

## Features

Almost all features are optional, and can be toggled in your configuration file:

* Horizontal or vertical navigation
* In-page navigation
* Keyword search
* Dark mode
* Datestamp
* Edit on Github
* Contact form
* Netlify CMS

- - -

## Who needs a spacebook?

A spacebook is for anybody who believes in the [\#indieweb](https://indieweb.org/) and wants a simple, modern, and free way to put a notebook-like thing on the web that they own and control:

* Writers and thinkers
* Planners and dreamers
* Technical doc writers
* Project managers
* Teachers and students

Anyone who is willing to learn a few simple things can create as many spacebooks as they'd like for any reason in the world.

- - -

## Installing spacebook

In theory, you can launch a spacebook without ever downloading the code or running your site locally. Just click the green Netlify button above and edit your files directly on Github! (The Github UI is fairly mobile friendly, and it is entirely possible to launch and manage a spacebook entirely via your phone :)) But if you want to customize your codebase or write your Markdown files in a local editor, you'll want to download and install your site locally.

### Requirements

You must be running **Node version 12 or higher** due to the Tailwind 2.0 release. I recommend using NVM to easily manage your Node versions if you need to switch back and forth between older versions.

* [Node](https://nodejs.org/)
* [NVM](https://github.com/nvm-sh/nvm) (optional)

**To find your current node version:**

```
node --version
```

### Step one

If already have a Github repository from an automated Netlify install, simply clone a copy of your repository:

```
git clone https://github.com/<your-username>/<your-repository>
```

If you just want to try this out locally, you can clone the Spacebook repository directly:

```
git clone https://github.com/broeker/spacebook
```

*Note: If you choose the second option, you'll need to remove the existing .git folder and add your own upstream repository if you want to use this as a basis for moving forward. You can also simply copy or [fork the repository](https://github.com/broeker/spacebook) directly from Github.*

### Step two

Install the site and run an initial build command:

```
cd spacebook

npm install

npm run build (only necessary the first time!)
```

*If you get errors here, double check your node version*

### Step three

Now spin up your local server to see your site:

```
npm run start
```

This command will start a local server and you'll be able to work on your site with hot reloads and some nice Browsersync features. If you install your site locally without connecting it to Netlify, you can easily do so later by moving your code into its own Github repository, and then creating a new Netlify site connected to that repository. 💥