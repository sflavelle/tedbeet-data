# Tedbeet (The General Chat) Discord Server Config

Configuration files for various bots we use in our Discord server. This is not of much use to anyone.

Our main Discord bot is called Bucket (a callback to our IRC bot of choice, courtesy of [XKCD's IRC channel](https://github.com/zigdon/xkcd-Bucket/)).

Our most noteworthy files are [red-serverquotes.json](red-serverquotes.json) and [red-triggers.json](red-triggers.json) - they contain the most expression of ourselves.

Many of these files store the unique data for our server for perusal, however there are four files that can be used freely:

- **cogs-dataIO.patch** - patch file for red-discordbot. Apply to the cogs/dataIO.py file. Doesn't create a new file every time the bot writes something. Handy for things like this GitHub repo where I can hard link the used files into the repo.
- **nodered-bucket-idlesystem.json** - Node-RED flow for our Idle message system. After a determined period of chat downtime (3 hours currently), Bucket will pick a random factoid, Bucket Fact, quote, or music jam, and post it in the chat.
- **nodered-bucket-inventorysystem.json** - WIP of the inventory system inspired by the XKCD Bucket software. Has two databases used by the JsonDB palette, /allitems and /helditems. Bucket can be given items, can rummage for items it knows (allitems), can list items it's holding (helditems), can give out items, and can remove items from its hand OR destroy/forget items that it knows about. *[nodered-bucket-inventory.json](nodered-bucket-inventory.json)* contains a snapshot of the inventory that we use.
- **nodered-bucket-quotenumlist.json** - simple script to extend Red. Reads the Discord client for the phrase 'lsquotes', Reads Red's serverquotes.json file and tells you how many quotes there are in total. 
