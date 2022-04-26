---
title: Setting Up & OpenVault
date: 2022-04-24 13:02:32
tags: coding
layout: default
---
Hi and welcome to my blog. Thought I should start blogging to document my journey about learning Java while working on [OpenVault][] and also talk about computer stuff.

This is going to be a long blog because I will be talking about everything leading up to OpenVault.

# Before PassVault

Before I started working on [PassVault][]. I was self-learning coding (JavaScript in this case) and needed to work on a real-project instead of a simple calculator or clock app.

The thought of making a password manager came up since I was having a hard time with memorizing multiple passwords and didn't want to use the same passwords for everything. I also don't like putting sensitive information in the hands of any company regardless of how big or small it is; and many companies pull an Adobe by making you sign up "for free!!" and then asking for your credit card information at the last step to start a trial. 

# PassVault

I started working on PassVault and learning JavaScript, Node.js, HTML and CSS at the same time. I think it was a pretty big undertaking for an absolute beginner but documentations and YouTube tutorials helped me out a lot.

Here's the [README](https://github.com/HamzaAlsarakbi/PassVault/blob/main/README.md) for PassVault if you want to know more about it.

## Problems with PassVault

Over time, especially after going to Carleton. I realized how the entire codebase was basically stitched together with functions. Which makes sense anyways because classes suck in JavaScript.

### JavaScript

I found JavaScript to be really weird, and quite slow. So I thought of moving all my code to TypeScript to get rid of the weirdness but the code is still slow because JavaScript is single-threaded which means it only runs on 1 thread.

### Electron

I used the [Electron](https://www.electronjs.org/) framework to build PassVault. The problem with it is that it's just a stripped down version of chromium with Node.js so it isn't a good fit for PassVault. Maybe web apps could definitely make use of Electron since they don't have to write a web and desktop version of their app like Trello, Discord, Slack, etc.

### Encryption

Instead of saving the data files raw. The code encrypts the file (`data.json`) and SAVES the encryption key in another file (`param.json`). So you can just get a hold of the key and data files and decrypt the data file.

Now I didn't really know any workaround at the time. So I just rolled with it. But still kept in mind that I will change it sometime later down the line.

### Other stuff

I took COMP 1406 (Introduction to Programming II) this winter and learned more about Object-Oriented programming. With that in mind, I realized that I can't keep working on PassVault and would just have to completely rewrite it.

Also I wanted to add features like saving keys (GitHub keys, Spotify keys, etc.) and with the already messy code-base, it is just better to start over and also JavaFX. So here comes OpenVault.


# OpenVault

I'm still not entirely sure about the naming. I thought of "PassVault II", "OpenManger". I don't have any creative names so I'm going with this for now and might change it before shipping v1.0.

## Java/IntelliJ

Not sure if this is a Java or IntelliJ issue, but sometimes my code just stops working for no reason even if I don't change anything. I get a random error and have to mess around in the `module-info.java` file until it works.

## JavaFX

My journy learning JavaFX has been quite interesting. I really miss the simple errors of Python or JavaScript. The stack trace is so long and finding a bug is hard and intimidating at first, but I think I know what to look for know and understand what errors are supposed to mean.

## UI

I was not sure whether I should use a UI library like Gluon or design everything from the ground up myself. Gluon feels like a 2016 android app and I wanted my app to look unique so I decided to go make my own UI controls.

Here are some photos:

![](../res/setting-up/2nd-ui.png)
This is the first iteration.
![](../res/setting-up/current-ui.png)


This is the current iteration. The UI is still a WIP but the sidebar is almost finished. I just need to remake the icons because I think they just don't look that good yet. Will probably add colors so that they stand out better.

On the right is the logins menu which holds all the passwords. It works almost the same as PassVault, except that the type of password is now a drop-down menu with the ability to add options. The stock options will be: `Personal`, `Work`, and `School`.

Right now, I'm working on a custom input controller where the label goes up when the user clicks on the text field. Still no animations yet but coming soon!

![](../res/setting-up/rich-input-demo.gif)

Also the red text is the error message if the user doesn't enter valid text in the a text field. Still working on the model for logins and the UI will be updated after that.

# Wrap up

Thanks for reading this blog. More will be on the way. Let me know what you think at hamzaalsarakbi@gmail.com!

[GitHub](https://github.com/HamzaAlsarakbi)


<!-- Links -->
[PassVault]: https://github.com/HamzaAlsarakbi/PassVault
[OpenVault]: https://github.com/HamzaAlsarakbi/OpenVault