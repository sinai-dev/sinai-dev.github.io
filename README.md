<p align="center">
<img align="center" src="https://i.imgur.com/DWezCnm.png">
</p>

The <b>Outward SideLoader</b> is an API and a tool for Mod Development in the game Outward. It is designed to simplify the process of creating new content and modifying existing content. SideLoader is capable of loading AssetBundles, Textures and Audio files, and can use custom XML files to make changes to game variables. SideLoader also offers a powerful C# API.

SideLoader elsewhere:
* [GitHub](https://github.com/sinaioutlander/Outward-Sideloader)
* [NexusMods](https://www.nexusmods.com/outward/mods/96)

### Installing {docsify-ignore}

* <b>[Latest Release](https://github.com/sinaioutlander/Outward-SideLoader/releases)</b>
* [How To Install](GettingStarted/Installation)

### Getting Started {docsify-ignore}

See these articles to get started making SL mods:
* [Overview](GettingStarted/Overview.md)
* [SL Packs](GettingStarted/SLPacks.md)
* [SL Menu](GettingStarted/SLMenu.md)
* [Guides & Examples](GettingStarted/Guides.md)

### External Links {docsify-ignore}

See these links for useful references, files, examples, etc:
* [Outward Tools](https://docs.google.com/spreadsheets/d/1btxPTmgeRqjhqC5dwpPXWd49-_tX_OVLN1Uvwv525K4/edit#gid=673914692) <i>(IDs, Tags, datamined info, etc).</i>
* [SideLoader Resources](https://github.com/sinaioutlander/Outward-SideLoader/tree/master/Resources) <i>(GitHub repo of some useful files)</i>

### Credits {docsify-ignore}

SideLoader is written by Sinai.

Discord: <b>Sinai#4637</b> (find me in the [Outward Discord](https://discord.gg/outward))

[Sinai's Mods Repo](https://github.com/sinaioutlander/Outward-Mods)

## Roadmap
This is a rough plan of the development of SideLoader. The order is not set in stone by any means.

<span style="color:red">*</span> = out of my control at the moment.

### v1.X
- [x] Texture Replacement
- [x] Audio Replacement
- [x] Custom Items
- [x] Item Visuals

### v2.X
- [x] Using BepInEx / Harmony
- [x] Re-write Custom Serializer
- [x] SL Template Generator
- [x] Item Extensions
- [x] Item Recipes
- [x] Skill Trees
- [x] Status Effects
- [x] Effect Serialization
  - [x] Effect Conditions
- [x] Characters
  - [ ] Savable Characters
  - [ ] SL_Summon Support
- [x] Custom Enchantments
- [x] Custom Tags (C#)
- [x] Hot Reloading
- [x] All supported SL_Item, SL_Effect and SL_EffectConditions

Maybe:
- [ ] Custom or Modified Blast/Projectile Visuals

### v3.X Ideas
SL 3.0 is probably a long way off, but my rough idea is:
- [ ] Improved SL Menu
  - [ ] Browser for loaded SL Packs
  - [ ] Editing SL templates
- [ ] Non-Human Characters <span style="color:red">*</span>
- [ ] Custom Props
- [ ] Custom Scenes
- [ ] Generic `UnityEngine.Transform` Serialization (to replace EffectTransforms and expand it)
- [ ] More robust Serializer (allow for UnityEngine classes, etc)
- [ ] Custom Status Families

Maybe:
- [ ] SkinnedMeshRenderer support <span style="color:red">*</span>
- [ ] XML Skill Trees / Skill Trainer setup
- [ ] XML Custom Tags
- [ ] Item Sources (adding items to merchants, droptables, etc)
- [ ] Custom Quests, or at least SL_Quest (SL_Item)
- [ ] Custom Dialogue / NodeCanvas Support