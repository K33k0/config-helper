# Day 1

I have a script that needs a couple of values replacing and pasting into a terminal. Easy enough... Turns out I'm not a fan of find and replace. 

My idea is to have a program that can read a file, then apply some kind of templating to it. Have a front end with some fields that will update the template.

I want this to work with any file. Maybe have a browse button or a drop down to scroll through files in a directory.

The app will check how many fields it requires. Adding the m to the interface where required.

As a stretch i'd like to add custom field requirements. Though it would tak more user config.

---------------

To start with I've looked into setting up an electron app, and how I would go about getting it compiled to an exe. Seems easy enough with electron forge.

Using the provided example gives me a good base to work off as well.

Next I will jump straight into reading a file with node and displaying on the the app. May as well start with the easy stuff.

Interestingly, I get a module not found error for fs. This is within the preload script though. I guess I need it to be in the main.js. Yes, moving the fire read into the main.js seems to work. At least it managed a console.log. 

Next up is displaying that output in the html body.

Turns out, I need to use inter-process communication. Should have probably learned more about electron before jumping in. Doesn't look to bad though, similar to web sockets. 

# Day 2

After realising what I was doing just wasn't working, I did a little extra reading and found a [link](https://github.com/reZach/secure-electron-template/blob/master/docs/newtoelectron.md) which is apparently a good way to create secure electron apps. I've read through the example, which seems to make a little sense. I'll be keeping it open for a while for reference. It remind a little of creating WPF interfaces in C# (painful).

Using the example, and making a couple minor tweaks, I can now output a txt file into the website