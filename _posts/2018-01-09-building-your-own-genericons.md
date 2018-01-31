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
When building this website, I ran into an issue: [Genericons][1], the font used to render the social logos in the sidebar, does not include an UpWork logo! I still wanted to link to my [UpWork profile][2], so I decided to build my own version of Genericons with an UpWork logo included.

I found [these instructions][3] for building Genericons, but I found the process to be cumbersome -- particularly on Windows. To make things slightly easier, I forked Genericons and replaced the existing build system with `grunt-webfont`. In the end I came up with [Genericons Grunt][4].

In this tutorial, I'll explain how you can use Genericons Grunt to build your own version of the Genericons icon font.

## Step 1: Install ttfautohint and fontforge

Genericons Grunt uses [FontForge][5] as a font rendering engine. It also depends on [ttfautohint][6] for hinting. The first thing we need to do is install these dependencies.

**OS X**

`brew install ttfautohint fontforge --with-python`

**Linux**

`sudo apt-get install ttfautohint fontforge`

**Windows**

1.  Download and install [ttfautohint][7].
2.  Download and install [FontForge][8].
3.  Add *C:\Program Files (x86)\FontForgeBuilds\bin* to your *PATH* environment variable.

## Step 2: Clone genericons-grunt

Now the fun part starts! First, let's clone the Genericons Grunt repo and cd into it.

    git clone https://github.com/bporcelli/genericons-grunt.git
    cd genericons-grunt    
    

## Step 3: Choose your icons

Next, we'll choose the icons for our version of Genericons. This is as easy as adding, editing, or removing SVG source files from the *svg* directory.

In my case, I'm going to drop in this [UpWork logo][9]. Note that icons you add should be aligned on a 16x16 px pixel grid for the best results.

## Step 4: Bake the font!

Finally, we get to build our icon font! It's as easy as running two commands:

    npm install
    npm run build
    

If all goes well, the *genericons* directory will now contain your customized Genericons font.

**Note for Windows users**

You may encounter a build error when running *npm install*. If so, install [Visual Studio 2015][10] and try again.

## Conclusion

Now you know how to build your own version of Genericons. If you have any questions or suggestions, please leave a comment below!      

 [1]: http://genericons.com
 [2]: https://www.upwork.com/fl/bporcelli
 [3]: https://github.com/Automattic/Genericons#building-your-own-genericons
 [4]: https://github.com/bporcelli/genericons-grunt
 [5]: http://fontforge.github.io/en-US/
 [6]: https://www.freetype.org/ttfautohint/index.html
 [7]: https://www.freetype.org/ttfautohint/index.html#download
 [8]: http://fontforge.github.io/en-US/downloads/windows/
 [9]: https://drive.google.com/open?id=1H1gqcfCj2hTBMCmDyVt_uEidm9AGHm0
 [10]: https://www.visualstudio.com/vs/older-downloads/