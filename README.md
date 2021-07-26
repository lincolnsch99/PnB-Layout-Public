# PnB-Layout-Public
Public repository for my Smite PnB Layout. Contains all the files available in the Google Drive ZIP folders, but using a repository is easier for some people.

# Licensing and Permissions
Anyone may use this application for their personal or business streams and may still accept any profit they make from said twitch channel; however, you cannot sell or profit from distributing this application directly in any way.
I am not responsible for any foul use of this product (eg. Inappropriate names/graphics used in the layout).

# Overview
This tool is just something I wanted to make so some of the lower-level Smite leagues could still create good content for everyone to see. It at least makes the stream look more professional when you have a good-looking pick/ban layout. With the way that resources are used in this application, I’ve tried to leave as much creativity open to you as possible. Almost everything shown in the display window can be changed visually, the only thing locked is the locations of the picks/bans. If you’d like, you can even make every element of the screen transparent except for the picks/bans and create an entirely different looking layout just using the picks/bans from the application. I’ve put way too much work into this thing just for me to only give it to the league I’m in, so please enjoy!

# Setting Up/Personalizing for your Usage
For the tool to allow you to customize as much as possible, I’ve made it so you can create your own team logos and other elements for the layout. All customizable elements are located in the Resources folder. For your first time installation, be sure to download the Resources.zip and extract it somewhere on your computer that you will remember. There are four main folders contained in your Resources folder:
- The “GodImages” folder contains all images used for each god’s pick and ban displays. You can edit these if you like but for best results just leave them as is.
- The “Display” folder contains images used for the different screens that this application provides. The main screen is obviously the “LayoutTemplate.png” since this is the background used for picks and bans. Change these by either loading it into some editing software such as photoshop and making your changes or simply replace them with a file with the same name.
- The “Sounds” folder contains, well, sounds. If you don’t like the voice lines that are used for each god when they’re picked, go ahead and replace the correct file with what you would like. The sound effect for when a ban is selected is called “hover.mp3”.
- The last folder is the “Teams” folder. By default, there are just two teams: Order and Chaos. For every team you want to add to the application you must create a folder with the team’s name. Inside each of the team folder there must be three files: Left.png, Right.png, and PnB.png. If they are named anything else, they won’t be recognized by the application. Use the sample .png files provided in the team’s folder to customize and to correctly size all elements. ***FOLDER NAMES CANNOT CONTAIN SYMBOLS***

# OBS Setup:
- If you haven’t already, be sure to download the Application.zip folder and extract somewhere that you will remember. This folder contains the actual application and .exe to run it. 
- After opening the application, two windows will pop up: the Display window and the Settings window. Using a “Window Capture” element in OBS, you can capture the Display window and resize it to whatever your resolution is. It’s default resolution should scale pretty well to the standard 1920x1080. The window is also where the sounds are played from, so I usually just have that detected on Desktop Audio in OBS. I’ve never done anything with audio splitting or stuff so if you’d like to do that then you’ll have to figure it out yourself. The settings window is what you will use to edit all the picks, bans, teams, set score, and other information so that won’t be displayed on OBS. This application works much better on dual monitor setups so you can have Smite on one screen and the settings window on the other, but if you must use only one screen then the settings window should be small enough to fit in the middle of the screen while still being able to view the picks and bans from Smite.
- In case you haven’t figured it out, you’ll basically spectate your smite game, then replicate what you see to the settings window so that anyone watching on stream will see the Display window updated. The goal of this project was to make this easy to use, so hopefully everything only takes a couple clicks to complete.

# Resources Setup:
- On your first time loading into the application, all the drop downs and other stuff will be empty in the settings window. To load in all your resources, simply click the browse button (little magnifying glass) next to the “Resources Path” display at the bottom of the settings window. It will open a little file explorer, and here is where you need to let the application know where your resources folder is. Once you’ve selected the correct folder, the settings window should update with all the gods, teams, and other info placed in the dropdowns. If you make changes to the resource files while the application is running, there is a chance that they won’t update in the application and could cause errors. If you make changes, be sure to hit the update button (circular arrow) next to the browse button to manually run an update on all the settings window elements.

# Changing Teams:
- At the very top of the settings window there are two drop down menus. Once you’ve set your resource path correctly, it should automatically fill in the dropdown menus with all your teams you’ve created. Select the correct teams in the dropdowns and the changes will be reflected in the display window.
- There are also some textboxes for the set scores. By default, it’s 0 – 0, just type in the textbox whatever you’d like to be reflected on the display window. If you just leave the textboxes blank, then nothing will be shown in the display window for set score.

# Picking Gods:
- There are five dropdowns for picks for each team. They are positioned in the same way that they will appear in the display window. To select a god, simply find them in the dropdown menu. If you have a dropdown selected and start typing, it will auto-scroll you to what you’ve typed in (eg. If I see that Janus is being picked, I can type “j-a-n” on my keyboard and hit enter, and Janus will be selected in the dropdown automatically. If you don’t want to bother with typing you can always just scroll through the dropdown, ordered alphabetically.
- Next to the dropdowns there’s also a checkmark to specify if the pick is locked in or not. These are always unchecked by default. If you select a god from the dropdown while the box is unchecked, the god will show up greyed-out in the display window until you lock it in. Picks sounds are not played until the lock-in checkmark is checked. If you don’t want to bother with pick hovers, you can just pre-check all of the lock in checkmarks and each pick will automatically be locked in when you select it in the dropdown.


# Banning Gods:
- Selecting a ban works the same way as selecting a pick, however you use the ban dropdowns instead, and there is no functionality for locking in. Both picks and bans have a “Reset” button that sets all the dropdowns to empty and checkboxes to unchecked.

# Player Names:
- On the far right of the settings window, there are ten textboxes for showing player names in the middle of the display window. Simply type in the player names and check the “Visible” checkbox if you’d like them to be displayed. This feature is still in the works, so I’d only use it if you don’t have anything else to put in the center of the layout. I’d highly recommend putting caster cameras or something else in the center of the pick/ban layout since it looks pretty empty otherwise. 

# Top Bans:
- The last section in the settings window contains functionality for the top bans portion of the layout. There is a simple button and checkbox. The checkbox is simply to display the current top ban data. Without sufficient data it likely won’t display correctly, so be sure to leave the checkbox unchecked if you do not plan on using this feature.
- The button is all you really need to use. What the button does is read the current team being displayed and what bans have been chosen and stores them in a .json file in the corresponding team’s folder. (To be specific, top bans are the bans against that team). This is all automatic and will give you a confirmation message before committing to it, because I currently don’t have functionality for undoing these unless you go in and do it manually. For displaying these top bans, all calculation is done automatically so there is nothing more you have to do after submitting all drafts for a team.
- The .json files that these stats are stored in are easily accessible in the team folders and can be shared to others if you want to have the same data. The guide video goes into much more detail and I highly recommend watching it.

# Future Additions/Features Being Worked On
## Integrating with other games
- I'd like to use this on other games such as League of Legends, DOTA, maybe even the new Pokemon Unite, or really any game with picks/bans really. 

If you have suggestions or bugs to report, please contact MeatyManLink#7738 on discord, or email lincolnsch99@outlook.com.
