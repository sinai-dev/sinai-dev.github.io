# Guides & Examples

This page contains some guides and examples to help you get started using SideLoader.

## My First SL Mod
First, have a quick read of the [SL Packs](GettingStarted/SLPacks) article to understand how to work with SideLoader from folders. No knowledge of C# is necessary for this.

Next, start Outward. We are going to use the [SL Menu](GettingStarted/SLMenu) to generate a template from an existing Item for us.

In game, press <b>Ctrl + Alt + F6</b> to open the SL Menu. In the Items panel, enter `2000010` as the Target Item ID, as well as the New Item ID. Press the button to generate the template.

Now, open the folder `Outward\Mods\SideLoader\_GENERATED\`, this is SideLoader's folder for generated templates. Inside here, you should see an `Items\` sub-folder, which should contain a folder called `2000010_IronSword\`.

<b>Cut</b> this Iron Sword folder (Ctrl+X), and go back to the `SideLoader\` folder. Create a new folder in here called `Test\`, create a sub-folder for Items (`Test\Items\`), and <b>Paste</b> (Ctrl+V) the Iron Sword folder in here. It should now look like this: `Outward\Mods\SideLoader\Test\Items\2000010_IronSword\`.

Have a look at the related article ([Custom Items](Custom/Items)) to get a better understanding of what you're looking at. There might be a lot of information, don't worry if you don't understand it all right away.

Now start editing the XML or the PNG files however you like. If you're not used to editing XML, there are various tools you can use online to help with editing and verifying it.

Start the game, and press F1 to open the in-game Debug Menu (requires a file called `DEBUG.txt` to exist in the folder `Outward\Outward_Data\`). Spawn the Iron Sword and have a look at your changes.

If there were any errors, SideLoader should log them in the file `Outward\output_log.txt`.

## WIP

Work-in-progress, please wait...