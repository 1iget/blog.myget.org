---
layout: post
title: "Get your local NuGet repository online in a private MyGet feed"
date: 2011-06-08 22:10:00 +0200
comments: true
published: true
categories: ["post"]
tags: ["Development", "Feature", "NuGet"]
alias: ["/post/2011/06/08/Get-your-local-NuGet-repository-online-in-a-private-MyGet-feed.aspx", "/post/2011/06/08/get-your-local-nuget-repository-online-in-a-private-myget-feed.aspx"]
author: "Maarten Balliauw"
redirect_from:
 - /post/2011/06/08/Get-your-local-NuGet-repository-online-in-a-private-MyGet-feed.aspx.html
 - /post/2011/06/08/get-your-local-nuget-repository-online-in-a-private-myget-feed.aspx.html
---

<p>One of the <a href="http://www.myget.org" target="_blank">MyGet</a> features I've been working on lately should make it easier to populate your private feed with the NuGet packages you want.</p>
<p>One of the specific use cases for MyGet is to be able to <strong>quickly set up a private feed with your own packages</strong>, which you might have in a local repository on your computer.</p>
<p>Before MyGet, you could make this feed available to other computers by sharing your repository for instance on a network drive, or by hosting your own NuGet server.</p>
<p>This required you to do some plumbing to get a server running, or to manage folder security settings, and above all, if a computer trying to consume the feed was not in the network, it could not get any packages from you repository.</p>
<p>MyGet provides you with a service (<em><a href="http://www.xavierdecoster.com/post/2011/05/31/Announcing-MyGet.aspx" target="_blank">NuGet-as-a-Service</a></em>) that allows you to easily host your private NuGet feeds and have it <strong>always accessible</strong> from any computer connected to the internet, <strong>without that setup hassle</strong>.</p>
<p>Since we launched, you were already able to upload a single package at a time to your feed. <a href="http://blog.maartenballiauw.be/post/2011/05/31/Creating-your-own-private-NuGet-feed-myget.aspx" target="_blank">Maarten extended this</a> with a simple checkbox to define whether or not you want to <strong>include its dependencies</strong>. Note that this dependency resolution only works for dependencies to packages on the official NuGet feed at the moment.</p>
<p>To facilitate the upload progress, I've now extended it to allow you to <strong>upload multiple packages at once</strong>.</p>
<div style="display: inline-block;"><img style="max-width: 600px;" src="/images/2012/2/multipkgupload.png" alt="multi-package-upload" /></div>
<p>This saves you again a couple of clicks and redirects!</p>
<p>When the packages are successfully uploaded to your feed, you'll get a nice notification telling you which packages have been added.</p>
<div style="display: inline-block;"><img style="max-width: 600px;" src="/images/2012/2/multipkguploadsuccess.png" alt="multi-package-upload success" /></div>
<p>Noticed that the above upload of 2 packages results in 3 packages being added? <em>(it resolved a dependency to elmah.corelibrary 1.2 for elmah 1.2.0.1)</em></p>

