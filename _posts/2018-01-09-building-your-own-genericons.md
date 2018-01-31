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
## Preface

When building this website, I ran into an issue: [Genericons][1], the font used to render the social logos in the sidebar, does not include an UpWork logo!

![Sidebar with UpWork logo missing.][2]

To get the sidebar rendering properly, I needed to build my own version of Genericons with an UpWork logo. Just in case you find yourself in a similar situation, I've described the process below.

## Getting Started

In this post, I demonstrate how to build a custom version of the Genericons icon font with [Genericons Grunt][3]. The process involves installing some dependencies, cloning a git repo, and running a couple of commands. Let's get started!

## Step 1: Install ttfautohint and fontforge

Genericons Grunt uses [FontForge][4] as a font rendering engine. It also depends on [ttfautohint][5] for hinting. The first thing we need to do is install these dependencies.

### OS X

`brew install ttfautohint fontforge --with-python`

### Linux

`sudo apt-get install ttfautohint fontforge`

### Windows

1.  Download and install [ttfautohint][6].
2.  Download and install [FontForge][7].
3.  Add *C:\Program Files (x86)\FontForgeBuilds\bin* to your *PATH* environment variable.

## Step 2: Clone genericons-grunt

Now the fun part starts! First, let's clone the Genericons Grunt repo and cd into it.

    git clone https://github.com/bporcelli/genericons-grunt.git
    cd genericons-grunt
    

## Step 3: Choose your icons

Next, we'll choose the icons for our version of Genericons. This is as easy as adding, editing, or removing SVG source files from the *svg* directory.

In my case, I'm going to drop in this [UpWork logo][8]. Note that icons you add should be aligned on a 16x16 px pixel grid for the best results.

## Step 4: Bake the font!

Finally, we get to build our icon font! It's as easy as running two commands:

    npm install
    npm run build
    

If all goes well, the *genericons* directory will now contain your customized Genericons font.

**Note for Windows users** You may encounter a build error when running *npm install*. If so, install <a href="https://www.visualstudio.com/vs/older-downloads/" target="_blank" rel="noopener">Visual Studio 2015</a> and try again.

## Conclusion

Now you know how to build your own version of Genericons. If you have any questions or suggestions, please leave a comment below!      

 [1]: http://genericons.com
 [2]: http://bporcelli.com/wp-content/uploads/2018/01/upwork-logo-missing.png
 [3]: https://github.com/bporcelli/genericons-grunt
 [4]: http://fontforge.github.io/en-US/
 [5]: https://www.freetype.org/ttfautohint/index.html
 [6]: https://www.freetype.org/ttfautohint/index.html#download
 [7]: http://fontforge.github.io/en-US/downloads/windows/
 [8]: https://drive.google.com/open?id=1H1gqcfCj2hTBMCmDyVt_uEidm9AGHm0