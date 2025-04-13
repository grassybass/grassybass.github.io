---
title: "Revamped This Site"
date: 2024-07-18T13:14:04+08:00
draft: false

description:

author:
  name: Yong Khang

hero: /images/revamped-this-site/didi.jpg
menu:
  sidebar:
    name: "Revamped This Site"
    identifier: revamped-this-site
    weight: 10
    parent: blog
tags:
  - Personal
---

## New Look!!

As you can see from my [first-post](../my-first-post-yay), I've revamped this portfolio with [another theme](https://github.com/hugo-toha/toha). IMHO this theme gives a better look and could present more information in a much cleaner way.


## The Process

Nonetheless this theme is a bit more complicated to set up, more so to <abbr title="you can't spell &quot;someone&quot; without &quot;me&quot;">someone</abbr> who had not messed with JAMStack before. Hence, I followed the simplest guide and modify their [sample project](https://github.com/hugo-toha/hugo-toha.github.io) to match what I wanted: fork the sample repo, clone it, modify it, push it, and let Cloudflare Pages built it.

Since I'm not using any content management software (CMS), I found it easier for me to just edit the markdown file using Notepad++, and have the Hugo server running in backgroup that automatically build with the latest content everytime I hit <kbd>CTRL + S</kbd>, and usually within 20ms!

Then I found out that I don't actually want Cloudflare to automatically building it from my repo. I only develope this site from my PC at home, and there's no collaboration of any sort. Granted, the version control would be useful to undo any mistakes, but it also add complexity for what is already less familiar to me, which would be more prone to mistakes.

Don't get me wrong, I'm very well happy learning new stuff, but for now, I just want to quickly get things done, since I resigned without a backup plan, sort of.

I then went on and built my resume using [Reactive Resume](https://rxresu.me), exported it as pdf, and threw it inside the assets folder and Hugo took care of the rest.


## The Limitation

While Cloudflare is kind enough to provide free JAMStack hosting, they have a limitation on the total file size per project of 25 MB. Previous theme gave my project a total size of 10MB, but this one is already sitting at 18 MB.

The first thing I've done to prepare for the future is to reduce the jpg quality of the images to about 80%, while also scaling down the resolution to 1200 x 900 px. This reduces the file size of each images to about 200 ~ 300 KB.

Then I remembered Cloudflare Images, which I could host my images there, which is excellent, since Cloudflare is a CDN and my assets would be served pretty quickly all over the globe.

But this <abbr title = "most likely doesn't, right?">doesn't</abbr> covers for other file type such as pdf. While my pdf is a measely 234 KB, I do want a future-proofing method before committing into a payment.


### Backblaze Saving the Day

Then I discovered that Backblaze also offers S3 compatible storage bucket, at a crazy cheap price of $6 per TB of data storage, with <abbr title = "up to 3x of total stored file size">free*</abbr> egress. They also have a free quota on storage, egress and operations which I wont be hitting any time soon:
  - First 10GB of storage/month is free!
  - First 1GB of daily egress is free!
  - Free Class A operations, and a <abbr title = "2500 each">hefty quota</abbr> of free Class B and C operation

The best of all? Backblaze is part of Cloudflare's [Bandwith Alliance](https://www.cloudflare.com/bandwidth-alliance/), which gives discount or even waived bandwidth fees between the members. This means that, if I get to have Cloudflare to serve their cache copy, instead of directly from Backblaze, it won't count toward even the free 1GB daily egress bandwidth!

I simply follow their [guide](https://www.backblaze.com/blog/free-image-hosting-with-cloudflare-transform-rules-and-backblaze-b2/) to set up my DNS records and apply some transform rules.

Then... done?


## Current Bottleneck and What's Next

No, sadly, not so fast. Remember that I said I modified their sample project instead of making on from scratch? That came back to bite me in an unexpected way. You see, the sample project only provide some of the files that the author thinks would be more useful to, well, newbies like me. Everything that you'll typically want to mess with, are all provided. But the core files, such as the HTMLs, would need to be pulled from the main repo as dependencies. While I get it that I can access those files in the AppData folder, I prefer to not mess with it right now.

The problem is that, the <abbr title = "aka Banner">hero image</abbr> is hard-coded to be served from local directory via `resources.Get`. And to load an image from a remote server, such as Backblaze, you'll need `resources.GetRemote` instead. With this limitation, I'd still have to stay put with lower image quality at the moment.

There's also this problem where I can't modify the color scheme, which causing dark theme to have low visibility on the "Activities" section of the homepage.

I could very well serve better quality images right now, as there are still about 6 MB of headroom and this site isn't very big. Since I plan to recreate this project from scratch by forking the main repo, and modify whatever code I need, I might as well only pump up the image quality by then. It's not like it's currently unbearable.


## Conclusion

All and all, this concludes yet another chapter of deploying JAMStack. In the next few weeks, I'll be busy job-hunting and listing more of my past projects here. So, the next "revamp" wouldn't be so soon.


## Who's That Siamese Cat?

Meet DiDi, a big and muscular but timid cat with some Siamese blood in him. He's about 4 months younger than [JuJu](../my-first-post-yay/#that-orimge-cat) but having a way larger physique (and appetite) than JuJu. Unlike JuJu, a natural alarm clock that powered by his hunger, DiDi is a much silent guy.
