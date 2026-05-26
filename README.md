## Note

This addon was not created by me, all credit goes to Nalfey for their hard work, I am simply providing a place for people to download it from. This has been done with Nalfey's permission.

# JSE
JSE (Job Specific Equipment) is an addon for FFXI that tracks the AF, Relic, and Empyrean gear you have and the next available upgrades. 
It looks for the NQ, +1, +2, +3, +4 versions that you have for a specific job and tells you which upgrade materials you already have / need to augment the JSE to the next stage.

## Commands

**`//jse [ af | relic | empy ] <JOB>`**
- Check equipment and available upgrades for a specific job, displays upgrade materials you already have or need to upgrade that job's equipment.

**`//jsetrack [ af | relic | empy ] <JOB>`** 
- Same as the basic //jse command but also displays in an extra, draggable window.

**`//jsetrack [ hide | show ] `**
- Hides/shows the //jsetrack window.  

**`//jseall af <JOB>`** 
- Specifically for AF Cards, this will check for gear on the currently logged-in character and also checks for cards on all charcters/mules that have an existing data file. (The addon must have been loaded once on that character for data to be available)

**`//jsecurrency`**
- Displays tracked currencies for upgrades and their values (Rem's Chapters, Gallimauffry, Apollyon and Temenos units)

**`//jsehelp`**
- Displays the available commands

## Examples ##

**/jse af WHM** - Displays needed materials to upgrade WHM Artifact armor
![jse_af_WHM](https://why-are-you-looking-at-an-image-url.dtrm.uk/img/nalfey-addons/JSE/jse1.png)

**//jsetrack af WHM** - Displays results in a draggable window
![jsetrack_af_WHM](https://why-are-you-looking-at-an-image-url.dtrm.uk/img/nalfey-addons/JSE/jse2.png)

**//jseall af PUP** - Checks for P. Cards on all your mules 
![jseall_af_PUP](https://why-are-you-looking-at-an-image-url.dtrm.uk/img/nalfey-addons/JSE/jse3.png)

**//jsecurrency** - Displays relevent currencies
![jsecurrency](https://why-are-you-looking-at-an-image-url.dtrm.uk/img/nalfey-addons/JSE/jse4.png)

### v1.11
* Syntax fix for some item name contractions.
* Extra tracking window code split into a separate file.

### v1.10
* Added a new command //jsetrack that displays the results in a dragable window. 
* Merged the //jse and //jsemats into a single command.
* Typo fix for SCH gear names and Maliya. Coral Orb.

### v1.01
* Minor display updates and syntax fix for DRG gear.

### v1.00
* First release.
