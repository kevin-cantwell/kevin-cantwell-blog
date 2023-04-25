---
layout: post
title:  "Bluesky Social"
date:   2023-04-24 22:03:15 -0400
categories: jekyll update
---
I recently got access to [Bluesky](https://bsky.app/) and it's...kind of ok! Very much like Twitter, but without the adoption (yet).

I especially like how they are handling verification with custom domains as handles.

## How it Works
The method requires a basic capability with DNS--which may prevent a large portion of users from making use of it. But technically,
it's a perfect way of verifying an account is who they say they are. As long as they have control over their DNS records, a recognizable domain
can claim that domain as their handle.

I followed their in-app instructions to set my own custom handle as the domain `kevin.cantwell.io`. The process is simple. You are asked to 
add a `TXT` record to your domain that holds a special value. As soon as Bluesky is able to query the record and validate the answer matches 
the value they specified, you're good to go!


![](/images/bluesky.png)
