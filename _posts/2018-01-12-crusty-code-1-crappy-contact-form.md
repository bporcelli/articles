---
ID: 315
post_title: 'Crusty Code: Part 1 &#8211; Crappy contact form'
author: bporcelli
post_excerpt: ""
layout: post
permalink: >
  http://bporcelli.com/2018/01/crusty-code-1-crappy-contact-form/
published: true
post_date: 2018-01-12 19:42:43
---
This is the first post in my <em>Crusty Code</em> series, in which I'll be reviewing and refactoring code I wrote in the past. Each post will feature a view of the code before and after refactoring along with an explanation of any changes made while refactoring.

Now that you know what to expect, let's get started!
<h2>Original code</h2>
For this post, I'll be reviewing a PHP contact form I wrote back in 2011. Here's the original code:

[github-embed config="https://github.com/bporcelli/crusty-code/blob/before/crappy-contact-form/.gh-embed.json"]

Oh, the humanity! Let's see what we can do to clean this mess up.
<h2>Changes</h2>
[github-changes owner="bporcelli" repo="crusty-code" from="fe22fc474a204a8d83972e8e67ba644f4861a632" to="d29285978890aef535f124df5ff1bbd46bb54e59"]
<h2>Refactored code</h2>
After all of those changes, here's what the code looks like:

[github-embed config="https://github.com/bporcelli/crusty-code/blob/after/crappy-contact-form/.gh-embed.json"]

It's far from perfect, but I think it's safe to say that it's better than what we started with.

Do you have suggestions for further improvements? Leave a comment below!