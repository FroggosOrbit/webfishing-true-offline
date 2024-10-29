# Webfishing True Offline/play
*For webfishingv1.08*

Currently webfishing's v1.08 of offline/solo play option still needs internet to start up. So I made a hard-patch that adds in a new button on the server screen to boot in a true offline mode, while not stripping away the online feature at all.

**This is a hard patch, and not a mod. A mod version will be made soon, and ill update this page with a link to that mod when its done**

# Current known mods that this patch doesn't work with
- none
  
*please message me on twitter or discord if you find a mod that should be on this list*

# WHAT YOU NEED TO INSTALL:
1: A legal version of the game (This patch uses the same check to see if you legally own the game that happens when you join servers, to also make sure you aren't able to load into an offline game if you dont own the game)
- Link: https://store.steampowered.com/app/3146520/WEBFISHING/

2: GDRE Tool (Used to decompile the game)
- Link: https://github.com/bruvzg/gdsdecomp/releases

3: GodotSteam v3.21 (How you run the game with this patch)
- Link: https://github.com/GodotSteam/GodotSteam/releases/tag/v3.21


# HOW TO INSTALL (Same for windows and steam deck outside of step 7):
*steam deck users must be in desktop mode for this*

1: Decompile the game using GDRE Tool
*Guide on how to decompile the game can be found as step one here: https://github.com/BlueberryWolf/WEBFISHINGModdingGuide*

2: Download the "Scenes.zip" from the release page of this github page
*Most recent release link:*

3: Extract "Scenes.zip"

4: Open the folder with the decompiled game, and drag the "Scenes" folder into the folder with the decompiled game.

5: On the pop up saying theres duplicate files, hit "replace all"

6: Download GodotSteam 3.21
- STEAM DECK USERS: Download "linux64-g352-s158-gs321.zip" , extract it, and then find and open "linux-352-editor". This is the program we will use to run the game with the patch

- WINDOWS: Download "win64-g352-s158-gs321.zip" , extract it, and then find and open "windows-352-editor-64bit". This is the program we will use to run the game with the patch

7: Drag your decompiled game folder onto the the godot window (godot = the "352-editor" program we just opened)

8: Once you see the webfishing option pop up in the godot menu, click it, and finally hit the "Run" button in the top right to play it

- EXTRA: Steam deck users can add the "linux-352-editor" to the gaming mode in steam to be able to use better custom controls. 

# IMPORTANT INFO:
- **The patched version of the game will still be able to use your normal save file, so you get a few items in offline mode, then boot up the non patched version in steam, you will still have those items**

- **This will not affect your steam download of the game in any way. This guide makes a copy of the game with the patch that runs through the godot program, instead of steam.**
- **The patched version of the game can play online without you having to do anything special, with it even connecting to your steam like the game normally does.**
- **The offline mode doesn't connect to your steam, which is where your in-game player get it's name from. So because the game can't give you a name, it just has it has "Null" when playing offline**

- *If you are thinking about porting the game to another platform, this patch will allow you to get around a lot of the issues related to actually getting the world and player to load in correctly offline. Ports will most likely have to be offline only, as the game is built with steam servers in mind*


# WHAT DOES THIS CHANGE IN DETAIL?
- Makes a new copy of your game to play with the patch, so it doesn't affect your steam version of the game
  
- This patch DOES NOT Cut off the NORMAL ONLINE features, so even though you dont play it through steam, it can still connect when you do one of the normal start game options
  
- Adds in a new button on the server screen that allows you to boot into a true offline mode
  
- This is done by adding a new flag in "Playerdata" that gets set to "True" once the new button is clicked. When that flag is set to true, it will ignore the timeout function that checks for an internet connection.
  
- This flag gets set back to "False" once you leave the game, allowing you to go back to playing online when you want
