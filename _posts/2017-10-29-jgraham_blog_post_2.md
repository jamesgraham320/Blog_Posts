---
layout: post
title:  "Easy blog hosting with jekyll"
date:   2017-10-29 18:36:51 -0400
---

**Intro to Jekyll**
-------------------

Contrary to popular belief, creating your own blog and hosting it is straightforward and easy. Using a ruby gem called Jekyll and github pages you can create a simple and customizable website to hold all your blogs. Documentation for Jekyll can be found [here!](https://jekyllrb.com) First things first, install Jekyll with 'gem install jekyll' to get started. After that you can generate a new website with the Jekyll new method. 

![jekyll creation](/images/jekyll_new.png)

And when you're done, your files should look a little like this:

![jekyll file structure](/images/jekyll_file_structure.png)

From this point, you can add new pages to your \_posts folder. The have to have a format of "yyyy-mm-dd-\<post\_name\>" which will help jekyll to arrange your posts in date order. Now that you're set up, we can look at some examples of Jekyll in action!

**Markdown (or HTML lite)**
--------------------------

Now that we've created a website and located where our posts are supposed to go, the next question is, how do we write a post? Thankfully there's a simple way to do that with a language called Markdown. Markdown uses simple syntax and a couple of symbols to effectively generate basic HTML. One thing to note is that all HTML is valid Markdown syntax, but in this case, it isn't necessary.
To get started with Markdown, all you have to do is end a filename with .md or .markdown. It works like a regular text file plus a couple extra options for formatting. Here's what it looks like: 

![some markdown](/images/markdown_example.png)

In the above example, you can see the layout of a markdown file (this one in fact). At the very top is the front information for Jekyll, this tells it the page information like the layout, title and date. Below that is the body of the markdown file. Anything between \*\* is bold, a dashed line denotes a secondary title and so on. There's a list of rules which show how simple it is [here!](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

**Hosting your site on Gitub Pages**
------------------------------------

This is the part that gave me the most trouble, but is actually pretty simple once you know what to do. Once your repository is pushed up to github, go to the settings tab and scroll down to Pages. Simply turn on pages by selecting the branch your website is on and make it generates a url for your web page!

![github pages example](/images/github_pages_example.png)

You can see near the top of the image it shows your url in a link. Click on that to see your website and link to it wherever you want. The thing that tripped me up the most was forgetting to put in the baseurl in the config.yml file, without it, the whole website broke so make sure you include it! Making changes is equally easy, changes you make are immediately done as soon as you commit and push.

![pesky devil](/images/config_baseurl.png)

This concludes our little foray into hosting your website on github, I still have a lot more to learn about creating my own custom CSS to really customize it, but a working website is out there on the internet, ready for you to get blogging.

-James Graham
