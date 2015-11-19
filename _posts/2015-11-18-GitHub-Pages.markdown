---
layout: post
title:  "GitHub Pages"
date:   2015-11-18
categories: site experiences editorial GitHub Jekyll
---

# Setting up GitHub Pages

Since I am running this simple blog on [GitHub Pages](https://pages.github.com/) I wanted to make my first "tech" article about my experiences with setting it up. Honestly it was a very straight forward setup and I didn't really run into any major hurtles save one but that was an SVG challenge and really had nothing to do with [GitHub Pages](https://pages.github.com/).

## Initial Thoughts

I had been playing around with the thought of starting up my own blog however I didn't want anything overly complicated, and for what I am trying to achieve with this site I didn't want to start with a paid site. I had played around a bit with [Jekyll](http://jekyllrb.com/) in the past after hearing about it on a podcast (to be honest I'm not sure which one, it might have been [Ruby Rouges](https://devchat.tv/ruby-rogues)) and I knew that [GitHub](https://github.com/) had the ability to host a static site. It seemed like a fun project to try out and so I carved out a bit of time to get started.

## Getting Started

The first step was to learn more about [GitHub Pages](https://pages.github.com/) and this page walked me though step by step. The first decision was to pick between an organization site or a project site.

The **Organization** site lives as project under your account and uses a special naming convention, *username.github.io*, where *username* is the account username. So for instance I created a project [patrickst1.github.io](https://github.com/patrickst1/patrickst1.github.io) under my account. You would use this type if you want one site to cover topics related to the account and not a single project.

However there are times when you need a site that is specific to an individual project and that is what the **Project** sites are for. Instead of being a project under an account the site is housed in a special branch, *gh-pages*, under the project.

Once you decide it is as simple as following the steps [GitHub Pages](https://pages.github.com/) has laid out and bada-boom bada-bing you have a site!

Well sort of...

## Adding [Jekyll](http://jekyllrb.com/)

Following along with the set of steps brought me to a place where I had an *index.html* page that displayed **Hello World**, as you do. What's next? Well at the bottom of the instruction page are three links to help with the next stage and one of them was getting [Jekyll](http://jekyllrb.com/) installed and running.

Again the site is full of great information however I skipped installing and setting up Jekyll since I already have it installed and the setup instructions are for creating a new [Jekyll](http://jekyllrb.com/) project. I had already cloned the project to my drive and had the git repo connected. Luckily [Jekyll](http://jekyllrb.com/) allows you to install a new site into an existing directory. So I created a new branch, deleted the example *index.html* page and used the following command inside the project directory to install a new Jekyll app.

```
  jekyll new .
```

As my son would say, "Easy, peezy, lemon, squeezy". I then wanted to test it out so I used,

```
jekyll serve
```

This serves the site locally at `http://localhost:4000` by default. I committed the changes and set off to start making the site my own.

## Making it my own

The first place was in the `_config.yml` file. This allows you to name your site, fill in some personal information, add a description, things like that. There is more but for starters I stuck with changing the default options. Since the site was still being served all I had to do was refresh the page and **boom!** there were my changes.

I also wanted to add a favicon so I placed a link in the `_includes/head.html` page and threw an image right in the root of the app. The next customization was a bit more involved and the first time that I really ran into trouble, but as I mentioned at the beginning this was more of an SVG issue than something with either [Jekyll](http://jekyllrb.com/) or [GitHub Pages](https://pages.github.com/).

I wanted to see if I could add links to [Stack Overflow](http://stackoverflow.com/) and [LinkedIn](https://www.linkedin.com/) using the same style as the GitHub and Twitter links. Once I figured out how to get the SVG images into the `_includes/footer.html` I was able to borrow from the existing links. Now if the sections are configured in the *_config.yml* both the [Stack Overflow](http://stackoverflow.com/) and [LinkedIn](https://www.linkedin.com/) links are displayed.

## Custom URL

The last customization that I added was a custom URL. My main registrar, [Hover](https://www.hover.com/) was having a sale so I thought that I would go grab one and wouldn't you know it, setting it up was, again, incredibly easy.

Once you have the domain, you point it at *username.github.io*. I used a CNAME for both `@` and `*`. The last step is to add a file named **CNAME** in the root of the site containing the new web address. For example mine has a single line, `pstachofsky.net` as the first (and only) line.

## Finishing it up

Once the site was how I wanted it I pushed all of my changes up to GitHub and created a pull request to merge them all into **master**. When I navigated to my custom domain, there was my site. Awesome!

Now I am rocking the default, basic theme. There are others or you can roll your own however that, I think is a project for another day.

Thanks for reading, I'd love to know your thoughts.

# Patrick
