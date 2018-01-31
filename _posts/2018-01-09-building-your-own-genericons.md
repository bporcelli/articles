---
ID: 291
post_title: Building your own version of Genericons
author: bporcelli
post_excerpt: ""
layout: post
permalink: >
  http://bporcelli.com/2018/01/building-your-own-genericons/
published: true
post_date: 2018-01-09 02:29:17
---
<h2>Preface</h2>
When building this website, I ran into an issue: <a href="http://genericons.com" target="_blank" rel="noopener">Genericons</a>, the font used to render the social logos in the sidebar, does not include an UpWork logo!

[caption id="attachment_294" align="aligncenter" width="285"]<img class="wp-image-294 size-full" src="http://bporcelli.com/wp-content/uploads/2018/01/upwork-logo-missing.png" alt="Sidebar with UpWork logo missing." width="285" height="81" /> Oh no! There's no UpWork logo :([/caption]

To get the sidebar rendering properly, I needed to build my own version of Genericons with an UpWork logo. Just in case you find yourself in a similar situation, I've described the process below.
<h2>Getting Started</h2>
In this post, I demonstrate how to build a custom version of the Genericons icon font with <a href="https://github.com/bporcelli/genericons-grunt" target="_blank" rel="noopener">Genericons Grunt</a>. The process involves installing some dependencies, cloning a git repo, and running a couple of commands. Let's get started!
<h2>Step 1: Install ttfautohint and fontforge</h2>
Genericons Grunt uses <a href="http://fontforge.github.io/en-US/" target="_blank" rel="noopener">FontForge</a> as a font rendering engine. It also depends on <a href="https://www.freetype.org/ttfautohint/index.html" target="_blank" rel="noopener">ttfautohint</a> for hinting. The first thing we need to do is install these dependencies.

<strong>OS X</strong>
<pre>brew install ttfautohint fontforge --with-python</pre>
<strong>Linux</strong>
<pre>sudo apt-get install ttfautohint fontforge</pre>
<strong>Windows</strong>
<ol>
 	<li>Download and install <a href="https://www.freetype.org/ttfautohint/index.html#download" target="_blank" rel="noopener">ttfautohint</a>.</li>
 	<li>Download and install <a href="http://fontforge.github.io/en-US/downloads/windows/" target="_blank" rel="noopener">FontForge</a>.</li>
 	<li>Add <em>C:\Program Files (x86)\FontForgeBuilds\bin</em> to your <em>PATH </em>environment variable.</li>
</ol>
<h2>Step 2: Clone genericons-grunt</h2>
Now the fun part starts!

First, let's clone the Genericons Grunt repo and cd into it.
<pre>git clone https://github.com/bporcelli/genericons-grunt.git
cd genericons-grunt</pre>
<h2>Step 3: Choose your icons</h2>
Next, we'll choose the icons for our version of Genericons. This is as easy as adding, editing, or removing SVG source files from the <em>svg</em> directory. In my case, I'm going to drop in this <a href="https://drive.google.com/open?id=1H1gqcfCj2hTBMCmDyVt_uEidm9AGHm02" target="_blank" rel="noopener">UpWork logo</a>.

Note that icons you add should be aligned on a 16x16 px pixel grid for the best results.
<h2>Step 4: Bake the font!</h2>
Finally, we get to build our icon font! It's as easy as running two commands:
<pre>npm install
npm run build</pre>
If all goes well, the <em>genericons</em> directory will now contain your customized Genericons font.

<strong>Note for Windows users</strong>

You may encounter a build error when running <em>npm install</em>. If so, install <a href="https://www.visualstudio.com/vs/older-downloads/" target="_blank" rel="noopener">Visual Studio 2015</a> and try again.
<h2>Conclusion</h2>
Now you know how to build your own version of Genericons. If you have any questions or suggestions, please leave a comment below!

&nbsp;

&nbsp;

&nbsp;