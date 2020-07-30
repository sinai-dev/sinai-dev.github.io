# Guides & Examples

This page contains some guides and examples to help you get started using SideLoader.

## Making a Custom Item
?> This guide introduces you to the concept of SL Packs, and shows you how to edit an Item.

Before we start, have a quick read of the [SL Packs](GettingStarted/SLPacks) article to understand how to work with SideLoader from folders. No knowledge of C# is necessary for this.

Next, start Outward. We are going to use the [SL Menu](GettingStarted/SLMenu) to generate a template from an existing Item for us.

1. In game, press <b>Ctrl + Alt + F6</b> to open the SL Menu. 
2. In the Items panel, enter `2000010` as the Target Item ID, as well as the New Item ID. 
3. Press the button to generate the template.

![Using the SL Menu.](https://i.imgur.com/5QQbJnn.png)

Let's find the template SideLoader generated.

1. Open `Outward\Mods\SideLoader\_GENERATED\`, this is where SideLoader generates templates to. 
2. Inside here, you should see an `Items\` sub-folder
3. Inside Items, you should see a folder called `2000010_IronSword\`.

![The `_GENERATED\` folder should look like this.](https://i.imgur.com/tqcQTzc.png)

Now we need to move this folder into our own SL Pack.

1. <b>Cut</b> this Iron Sword folder (Ctrl+X)
2. Go back to the `SideLoader\` folder. Create a new folder in here called `Test\`. 
3. Create a sub-folder in Test called Items (`Test\Items\`)
4. <b>Paste</b> (Ctrl+V) the Iron Sword folder in here. 

It should now look like this: `Outward\Mods\SideLoader\Test\Items\2000010_IronSword\`.

![Moving the folder to our own SL Pack.](https://i.imgur.com/gjxhoWk.png)

Have a look at the related article ([Custom Items](Custom/Items)) to get a better understanding of what you're looking at. There might be a lot of information, don't worry if you don't understand it all right away.

Now, open the `2000010_IronSword\Iron Sword.xml` file and have a look. Let's do something simple to start with and change the `<Description />`.

![The SL_Item XML file should look something like this.](https://i.imgur.com/zfrmzTJ.png)

To set a value, we will need to expand the brackets. Replace the value with this: `<Description>Test.</Description>`. 

![Setting a new description.](https://i.imgur.com/g14TBOZ.png)

Start the game, and press F1 to open the in-game Debug Menu (requires a file called `DEBUG.txt` to exist in the folder `Outward\Outward_Data\`). Spawn the Iron Sword and have a look at your changes, our description should now be set.

![It worked!](https://i.imgur.com/UxuA8ky.png)

If there were any errors, SideLoader should log them in the file `Outward\output_log.txt`.

## Replacing Basic Assets

?> This guide shows you an example of how you can replace simple assets (Audio / Music).

First, let's replace some music. Pick any song you want to use and make sure it is a `.wav` file (there are many free online converters for this if you need one).

Create a Test SL Pack (`Outward\Mods\SideLoader\Test\`), and create a `AudioClip\` sub-folder inside it. Put your `.wav` file inside the `AudioClip\` sub-folder (for example, `Test\AudioClip\MySong.wav`).

Next, rename your audio clip so that it matches the name of an existing audio clip. For this example, we will use the title screen music. Rename your audio clip to `BGM_GeneralTitleScreen.wav`.

Start the game, and you should now hear your audio clip.

For textures (not including certain menu assets), you can replace them in the same fashion with `.png` files. Put the texture `.png` file in the `Texture2D\` sub-folder of your pack. To get the name of a texture for replacement, see [this article](Replacing/Textures?id=finding-textures).

## Examples

See these links for more examples (these are existing SL mods):

A <span style="color:red">*</span> indicates that the source code may not be visible or easily accessible.

### Items
* [Imbued Bows & Mana Bow](https://www.nexusmods.com/outward/mods/106)
* [Arrows](https://www.nexusmods.com/outward/mods/130)
* [Crusader's Item Pack](https://www.nexusmods.com/outward/mods/134) <span style="color:red">*</span>
* [Radiant Damage Gear](https://www.nexusmods.com/outward/mods/135) <span style="color:red">*</span>
* [Runic Scrolls](https://www.nexusmods.com/outward/mods/132) <span style="color:red">*</span>
* [Holy Avenger Item Pack](https://www.nexusmods.com/outward/mods/128) <span style="color:red">*</span>

### Skills
* [Necromancy Skills](https://www.nexusmods.com/outward/mods/105)
* [Unlimited Rune Works](https://www.nexusmods.com/outward/mods/157)
* [Skilled at Sitting](https://www.nexusmods.com/outward/mods/127) <span style="color:red">*</span>
* [The Juggernaut](https://www.nexusmods.com/outward/mods/143) <span style="color:red">*</span>
* [The Templar](https://www.nexusmods.com/outward/mods/136) <span style="color:red">*</span>

### Textures
* [Antiquated Antiques](https://www.nexusmods.com/outward/mods/154)
* [Twilight Kintsugi Armor](https://www.nexusmods.com/outward/mods/147)

### Status Effects
* [Protection Bubble Shield](https://www.nexusmods.com/outward/mods/150)

## WIP

Work-in-progress, please wait...