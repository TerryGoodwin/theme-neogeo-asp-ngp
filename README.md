# theme-neogeo-asp-ngp
Theme and game card images for a NeoGeo Pocket system on the NeoGeo Arcade Stick Pro

This is for use with an ASP that has already been hacked with the HyloStick (or similar)
hack and at present, RetroArch is expected to also be installed to be able to play
Neo Geo Pocket games.

This does not include any ROMs or anything to help you hack the system.

Game card artwork is included only for the games I was personally interested in playing
on the system. As such, this is not a complete collection of cards, but if you want to add
your own a template has been included to do so!

# What it looks like

An example card:  
![alt text](https://raw.githubusercontent.com/TerryGoodwin/theme-neogeo-asp-ngp/main/ASPh/games/ngpc_samsho2/cover.png "Samurai Shodown! 2 card")

A crude photo taken from the TV of the theme in action:  
![alt text](https://raw.githubusercontent.com/TerryGoodwin/theme-neogeo-asp-ngp/main/photo_inaction.png "Photo from the TV")

# Before you start!

Make a backup of your `ASPh` directory before making any changes! It's very easy to mess
something up - if you do, you could end up bricking your ASP, getting it into a state
where it can't boot and will be stuck in a loop. If this happens, put EVERYTHING back
to how it was on your USB stick. If you still can't boot into the Hylo hack, boot into
the original, stock games and change the language to something that corresponds to your
hacked `lang_array.ini` for a system that you know was working fine.

# How to install

If you don't already have a script to launch NeoGeo Pocket games through RetroArch, copy
the file `retroarch\bin\ngp` to your existing `retroarch\bin` directory. If you do already
have a script, the `emuinfo.txt` stuff included here and explained further down expects
your script to launch NeoGeo Pocket games to be called `ngp` - if it's not, you'll need
to make adjustments to the `emuinfo.txt` and `rominfo.txt` files to reflect this
difference...

From your existing `ASPh\local` directory, go into one of the existing system directories
(e.g. `English`) and copy the `help` directory to the `ASPh\local\French` directory
included here.

In your existing `ASPh\local\lang_array.ini`, decide which of your existing systems is
designated as for the Neo Geo Pocket - if you have a full list of systems already as
default with the HyloStick hack, you'll probably have to replace one of them.

Look in the `ASPh\local\lang_array.ini` included here and copy the system name string:
`<NEO•GEO Pocket>`

And replace the system of your choice.

Rename the directory `ASPh\local\French` with the language name next to what you just
pasted into your `lang_array.ini` so they match.

Remember what line it is in your `lang_array.ini` file - this is important. For example,
if you're replacing French that is the third line. For our purposes we start with `0`, so
the third line makes it index `2` - this is needed for the next part.

Look in the directory `ASPh\image` included here, and replace the `2` with the number
you got above for both the file `global_bg_2.png` and the directory `main\game_focus_2`

If you don't already have the system set up to play Neo Geo Pocket games, once you have
RetroArch installed, look in `ASPh\hack\emuinfo.txt` included here and copy the two lines
to the bottom of your `emuinfo.txt` file - then delete the one included here.

Edit the file `ASPh\hack\rominfo.txt` included here, then copy the contents to the bottom
of your `rominfo.txt` file. Keep the IDs the same, just change the PATHs as necessary.
Once you've copied the information to your existing `rominfo.txt`, delete the file
included here.

Edit the file `ASPh\local\French\games.ini` file (NOTE: it may not be French depending on
what you did above) and update the list to reflect any changes you may have made (e.g.
removed some ROMs from the list that you don't have or don't care about) but make sure
not to change the `DIR` entries - but DO make sure you fix the `ID` entries so they still
run consecutively.

IMPORTANT! At this point these files...

`ASPh\hack\emuinfo.txt`  
`ASPh\hack\rominfo.txt`

...should not be present except in your existing file structure on your USB device or
wherever, you should have deleted the new ones as instructed above!

Copy and paste the entire `ASPh` directory included here, modified to the above
instructions, over your existing `ASPh` directory to merge the two together. IMPORTANT:
You really should have made a backup before this point!

Now when you boot into the hack on the ASP, the Systems option should have a
`NEO•GEO Pocket` option, which you can switch to for a new, clean NGP inspired
presentation and a nicely populated list of game cards!

# Making your own cards

A Pixelmator document is included (`template.pxm`) if you want to make your own cards.
Before exporting to PNG, your image should be resized to `286x321` pixels.

Have a look at the directory structures and ini files included here to see how it all
works and how things relate to each other - it's pretty simple so you should be able to
figure it out!

# Copyright stuff

Obviously I don't own any of the original game artwork or original iconography included
here. I created the theme background from scratch, but the game artwork and any logos etc.
all belong to their original creators.