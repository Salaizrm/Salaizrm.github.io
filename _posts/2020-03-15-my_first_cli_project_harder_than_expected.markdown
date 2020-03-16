---
layout: post
title:      "My First CLI Project: Harder than expected"
date:       2020-03-16 02:50:55 +0000
permalink:  my_first_cli_project_harder_than_expected
---


When I first saw this project it quickly overwhelmed me, this was not like any of the other lessons I was use to. However, after doing some research and watching the video provided (numerous times) on how to get started I felt it bit more at ease... Except when I finally started my project.

Probably the first 8 hours was learning new things and fighting with the Learn IDE 3 client. I did, at first, use the Learn browser client but quickly got annoyed when it crashed numerous times on me. The things i learned from this are from little too big. From simply things like learning I need to save with (ctrl + s) every few seconds, since the client doesn’t autosave like I’m used to in the browser version to being able to construct a scraper that doesn’t rely on hashes to grab data and show it to the user. 

This is my project: 
https://youtu.be/2VHdatQmlkE

Sadly, I wasn’t able to finish my project. I was able to get some of the program to function but other aspects of it need to be finished in order to call it complete.

first, I’d like to address some things that gave me a lot of trouble so that hopefully you the reader, can avoid these headaches:

- first, off if you followed the instructions on how to create your gem that were provided, awesome. but try to avoid putting a "dash (-)” when naming your project. it'll just create an extra folder with your version folder located in it, then you'll have to clean up a little before you even start your project (your already going to have to clean up quite a bit, might as well mitigate the damage).

![](https://imgur.com/r13Qrb8)
![](https://imgur.com/hOfJhN6)

- second, go to your gemspec file it should look like this: 

![](https://imgur.com/bqbglU8)

Alright now go ahead and fill in what you can and delete these:

![](https://imgur.com/IsNwvXt)

if you don’t delete these and fill in the TODO's, then anytime you run a test ruby going to let you know that none of those are filled out and stop you from progressing. 
Also: spec.add_development_dependency "nokogiri" and spec.add_development_dependency "pry". You do this so it knows to use Nokogiri and Pry. 

-third, watch the very instructional video on how to actually start coding your project located on the CLI Data Gem Portfolio Project lab.

-fourth, if your using the learn IDE 3 client, remember you'll always be dropped into Temporary. Make sure to enter in your terminal: cd your-project-name

![](https://imgur.com/E2qo82h)

you can use this to go deeper into your folders, very useful tool. but if you go too deep make sure to enter: cd .. 
this will get you out.

oh, and one last thing, remember to save often and always.

(Losing progress is quite depressing due to a power-outage (believe me, I know firsthand).

now that those are out of the way, I’d like to show you how I created the scraper that grabs the info for my CLI. Hopefully this will give you a head start to complete your project and save some sanity. A reminder, this is how i built my scraper. yours could very well differ and not one scrape method is a one size fit all for every project.

![](https://imgur.com/1I30RNp)

I defined my scrape method as def self.scrape_month
at first I only had the first loop |r|, after not being able to scrape from it I was lost for a long time, finally I asked for help and a teacher (Juan, very smart dude), was able to show me how to scrape all the data i needed to. since I was scraping from a list of objects that all shared the same "div.ds-main"

![](https://imgur.com/ZstDtyl)

I had to go further in the loop and to (".calendar-entry"). I highly recommend putting a binding.pry down before each thing you want to pull to make sure its pulling correctly, if at all. 

![](https://imgur.com/XAlhq77)

This is my games.rb file, this file allows me to store and call upon all the things my scraper stored.


If your having trouble calling on the binding.pry, don’t worry you’re not alone. again, another reason why this took so long to figure out was because I couldn’t even figure out how to test my own code (embarrassing I know). But hey we all fail at times and that’s ok, we just have to keep moving forward, no matter the challenge presented, albeit complicated or mundane. 

to test your own code, watch the video provided to make sure you have set up all the necessary 'requires' and 'require_relative'. Next, open your console ./bin/console, it'll tell you you don’t have permission to access. to get around this type in your terminal 'cd bin/' this will put you in your bin folder, next enter ls -lah you should get something like this:

![](https://imgur.com/Xz8MB6b)

next enter in chmod +x "name of file"
for the example provided with the picture above you'd enter chmod +x daily-deal

sweet, you should have access now. you will have to do this with all your files by the way.

I hope this was useful for you! I wish I could show you how to do it all but alas each project will vary and sadly I didn’t complete mine fully.

Good Luck and keep pushing forward!

-Robert Salaiz



