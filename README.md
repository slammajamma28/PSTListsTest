# PSTLists

This project aims to make tracking progress on Custom Trophy Lists on PlayStationTrophies.org simple and easy. I took this over from Noid, who ran and hosted this code for several years. Special thanks to Noid for his years of contributions!

## NEW SITE!

Since Noid will be shuting down his old site, he encouraged me to get this hosted. I was somewhat unaware of how easy it is to host a website on GitHub... so here it be.

https://slammajamma28.github.io/PSTCTL_V2/app/index.html

## NEW FEATURES!

### By Games Calculation "Fix"

I noticed that when checking off trophies on the "By Games" page, the counts for the lists do not update in the overview. So, I implemented the "Calculate" button. After you finish checking trophies off through the By Game page, refresh to get back to the Overview. Click "Calculate" and refresh the page again. The numbers should be updated accordingly.

### By Games Owned Games

One thing I liked about this tracking was the ability to see what games I owned in any individual list. But, having to go through each list individually was a chore. So I added a new box tot the By Games Page. There is a checkbox next to each game that will mark the game as owned. These games will be reflected appropriately when opening individual lists.

### Import / Export List Progress

Having seen a few people mention issues with losing progress for various reasons, I thought it would be a swell idea to have a way to save off progress locally. And that is what the Export button will allow you to do. Once you have done major updates your list, you can now use Export to get a bunch of text that represents your Local Storage progress. Save this text into a text file somewhere. 

If you lose your information or want to move your progress to a new computer/browser, you can use the Import button to refresh your information. Press the Import button, paste the text from your saved Exported file, press Import and your data should be restored!


## Old README info

For historical sake...

## What it does

Users first choose a list from the dropdown menu which they wish to track progress on. They can then check off which trophies they've earned as well as the games they own. This information is immediately (onclick) stored in HTML5 localStorage, and is shared across lists. So if you check "Game A" on "List X", "Game A" will also be checked off for you on "List Y" (all lists containing that game).

Users who have saved their progress may click on the "BBCode" button to receive the BBCode require to sign up their progress on the site.

## What's the tech?

### Jquery

I previously was using Angular for this project, but decided to rebuild it with JQuery. I was learning Angular through this project, and while I feel that I have indeed learned much, part of that learning is that I was doing it horribly. I'll continue to use Angular in other projects, but since this is used by a large number of people, I will be using JQuery since I can (at this time) make more updates faster with the code I already know through previous experience.

### Lists

The lists themselves are contained in a scope array in lists.js. Each list currently has a name, banner, and award image. Each trophy in the list contains the game name, trophy name, trophy description, and trophy image/icon.

### Sass

The site uses Sass for it's styles.
