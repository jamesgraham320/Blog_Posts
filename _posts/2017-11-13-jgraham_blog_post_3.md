---
layout: post
title:  "Vim modes and why they matter"
date:   2017-11-13
---

**Vim Modes and why they matter**
-------------------

Vim is an editor that many see as cryptic and difficult to understand. I just want to shed a little bit of light on the foundation of vim so that everybody can have a basic understanding of how it works so that next time you see it, you won't get confused as to why you can't type. 
As an editor, Vim revolves around never taking your hands off the keyboard, and the way that you do that is through very extensive shortcuts and plugins. The goal of this blog is to give a simple intro to how vim is set up.
Vim is based on three modes. Normal, Visual, and Insert mode. The three modes can be summarized as follows:

| Mode  | Description |
| ------------- | ------------- |
| Normal  | Use the keyboard to do commands  |
| Visual  | Use the keyboard to highlight text  |
| Insert  | Type normally  |


**Normal Mode**
---------------
You're gonna spend a majority of your time in normal mode. Pretty much every keyboard. It's the default mode when you open vim. Although vim doesn't have any fancy graphics, its always doing something behind the scenes. I personally keep a running text file to keep track of every command that I learn. 

[my notes](https://image.ibb.co/bJTnnb/Screen_Shot_2017_11_13_at_12_34_17_PM.png)

Almost every key is mapped to something different. In normal mode, p is paste, u is undoi, w is forward one word and so on. Vim also supports combinations of commands. For example if you press c + i + w, vim will delete the word you're inside of and put you into insert mode. If you're inside a set of quotes, you can try c + i + " and it will delete whatever is in the quotes and enter insert mode. C + i denotes that you want to 'change' 'inside' and whatever comes after denotes what you're inside ('w - word' '" - quotes').

**Visual Mode**
---------------

Visual mode is pretty straightforward. When in normal mode, press v to enter visual mode. In this mode, navigating with h, j, k, and l will move your cursor and highlight everything in between. This is synonymous with highlighting in an ordinary editor. Vim, however, offers a few ways to enter visual mode. Shift + v highlights your current line, and Ctrl + v will create a block highlight. These offer a lot of flexibility in how you highlight and edit your text.

**Insert Mode**
---------------

Insert mode can be considered the default of any other text editor. To anyone that is new to vim, the most basic way to start editing someones file is to press a or i. A will move the cursor forward one and begin editing, and i will start editing exactly where the cursor is. Once you enter insert mode you can type normally.
Insert mode is much more interesting when it interacts with the other three modes. Highlight a block of text in visual mode and press c to delete it and enter insert mode ('change'), Press o when in normal mode and skip to the next line and enter insert mode. Vim removes a lot of simplicity in the form of clicking around with the mouse, in favor of having countless options to configure how you tackle any option. 
