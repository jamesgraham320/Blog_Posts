---
layout: post
title:  "Feeling sassy"
date:   2017-12-10
---

Feeling Sassy
------------------------------

Sometimes CSS decides that it doesn't want to work. For when it starts acting up you have to give it a little bit of attitude and whip it back into shape. Luckily some smart people created Sass. It's a much more dynamic version of CSS that saves you time and effort. This sounds good, but you might ask, why would a styling language need dynaimc features? Take a look at these two sets of CSS and SCSS. Which would you rather look at and edit?

![SCSS File](https://image.ibb.co/gdEGvG/Screen_Shot_2017_12_10_at_3_30_52_PM.png)

![Compiled CSS File](https://image.ibb.co/gY1J9b/Screen_Shot_2017_12_10_at_3_31_18_PM.png)

This CSS comes from [CSS Shake](https://codepen.io/jamesmgraham320/pen/eewpMm). Someone created the styling that you can add to your own files to add this specific animation to any element you want. If you look at the SCSS file, it's about 415 lines long. This is a lot for one person to write but if you compare it to the over 1700 lines in the compiled CSS file, you can see how Sass can save you a lot of time and effort. 
For now lets took at a super basic example. Sass allows you to create variables and use them in your stylings. One of the most useful examples of this is colors. Most of us can't think in hexcode or RGB values so remembering which color is which in your styling can be pretty difficult. Much like any other language, Sass gives us functionality to save those colors to variables to be referenced later. 

![Sass color references](https://image.ibb.co/niC0pb/Screen_Shot_2017_12_10_at_4_11_44_PM.png)

In my own personal website, I have a bunch of colors that I have to refer to regularly. If i went around copying and pasting hexcodes and RGB values everywhere I would quickly become lost. By saving them to variables, it's much easier to keep track of all of them!

The last important feature of Sass we're going to talk about are mixins. These work similarly to just plain variables but you can save multiple style rules for use later with these. Many mixins are 'included' from other sources and generate common CSS for you (seeing a trend here?).

![Sass font-face mixin](https://image.ibb.co/jt9GvG/Screen_Shot_2017_12_10_at_4_18_09_PM.png)

This is an example of how you would include your font files. Normally you would have to declare each font file and their extension, but with a mixin, you can generate all of the basic file type endings you need. With only the path to the font files and the name of the font family, Sass can do the rest!
