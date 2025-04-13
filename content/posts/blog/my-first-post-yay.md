---
title: "My First Post Yay!"
date: 2024-07-05T04:50:08+08:00
draft: false

description: "First post on my own portfolio woohoo"

author:
  name: Yong Khang

hero: /images/jujuballs.jpg
menu:
  sidebar:
    name: My First Post Yay!
    identifier: my-first-post-yay
    weight: 10
    parent: blog
tags:
  - Personal
  - JAMStack
  - HUGO
  - Cloudflare
---
## Hello

"Hello World!" would be less precise here, so...

> Hello Internet!!

As of the writing of this post, I still not yet finished replacing all the default texts (or the lorem ipsums) into real content yet. But I just wanted to create this first post to commemorate the creation of this site.


## Why This Site?

So, why did / am I making this site?

This site is intended to be my portfolio as it would be. When it's done, you'll be able to have a good understanding on what projects I was being involved in.

In the future, I'll also be posting about random ~sh~stuffs that piqued my interests.

Cats, bass guitar, audio equipments, nice software, homelab stuff such as Hyper-V & Docker, privacy related stuff, password security stuff, or maybe even shitposts.

Not that I'm pro in any of these field, but I enjoy declaring myself as jack-of-all-trades.

### Why the Technicalities

You could argue that I'm a Game Designer, not a Web Developer, so I could've just created a portfolio with [WixSite](https://www.wix.com/portfolio-website), as what many others are doing, and call it a day.

I had thought about it. Until I saw the free tier doesn't allow me to use my custom domain that's it.

You see, I'd want my site looks more professional by having a custom domain name. They're cheap, a ".com" costs only about $9 a year on Cloudflare. Yes, you [CAN register a domain on Cloudflare](https://developers.cloudflare.com/registrar/get-started/register-domain/), at cost. Further more, I am somewhat familiar with Cloudflare and they have this [Cloudflare Pages](https://pages.cloudflare.com) thingy where you can host your JAMStack for free.

## How I Made This
> Or "making", depending on when are you viewing this site
This site is being created as a JAMStack. JAM stands for JavaScript, API, and Markup. This is a very efficient method to create a static website to serve to users. JAMStacks are often being hosted on Content Delivery Networks (CDNs) so they're generally zapping fast.

For example, this site is being generated with a Static Site Generator (SSG) called HUGO, running locally on my PC at home. Then I grabbed a [theme](https://github.com/gurusabarish/hugo-profile), some extra [add-ons](https://hugocodex.org/add-ons/), change some minor behavior, and I'm ready to write some markdown files to feed it into Hugo. Then Hugo would generate a folder with all I need for a JAMStack. Did I mention on-the-fly?

![build-hugo](/images/my-first-post-yay/build-hugo.jpg)

I've not yet linked it to my GitHub, so as for now I'll need to zip it up and upload it to the Cloudflare Pages, and BAM!! Cloudflare would host it for me, on my own domain.

It does have a maximum limite of 20,000 files and 25MB total file size tho, but I'll figure something out when I'm about to hit it.

In the future I might use some Content Management System (CMS) to properly organize my posts, but as for now I just want to quickly get the basics done.

## That Orimge Cat?

He's JuJu, pronounced as "GG". He's a noisy bastard that'd only meow for foods. I'll probably tell you more about my hellspawns in the future.

Right now, I'll have to zip up the build and throw it up into the Cloudflare to update this site. It's 4:50am now LMAO

