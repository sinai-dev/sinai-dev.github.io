# Custom Status Effects

<b>Custom Status Effects</b> can be used to make completely new Status Effects and Imbues or modify existing ones. You can do this either from an SL Pack, or directly from your own C# mod.

The SL Pack sub-folder for custom Status Effects is `StatusEffects\`.

## Creating a template

Use the <b>[SideLoader Menu](GettingStarted/SLMenu)</b> to generate templates for you from existing Status Effects or Imbues. It will also dump the icon and set it up in an SLPack structure ready to go for you.

Note - to get the ID of a Status Effect to clone from, use [this Google Sheet](https://docs.google.com/spreadsheets/d/1btxPTmgeRqjhqC5dwpPXWd49-_tX_OVLN1Uvwv525K4/edit#gid=1969601658) - find your effect on the list. For Status Effects, use the "Identifier Name", for Imbue Effects use the number to the left of it.

Pick a Status Effect similar to what you want to make (or pick the Status Effect you want to edit), and generate a template for it.

Your custom status XML can be placed in the `StatusEffects\` sub-folder of your [SL Pack](GettingStarted/SLPacks). The XML can be named anything.
* Eg, `[SLPack Folder]\StatusEffects\MyStatus.xml`

If you want to use a custom icon, you need to create a <b>sub-folder for each status</b>.
* Eg, `[SLPack Folder]\StatusEffects\MyStatus\MyStatus.xml`
* The icon needs to be called <b>icon.png</b> and placed in this same folder as the xml.

## Editing Etiquette

If you are editing <b>existing Status Effects</b>, see [the Editing Etiquette section](GettingStarted/Overview.md) on the SL_Item page about editing etiquette. The same rules apply to Status Effects and Imbues too.

On <b>SL_StatusEffect</b>, you need to set the TargetStatusIdentifier, and you need to set both the NewStatusID and the StatusIdentifier.

On <b>SL_ImbueEffect</b>, you need to set the TargetStatusID and the NewStatusID.

## SL_StatusEffect

`TargetStatusIdentifier` (string) <b>[REQUIRED]</b>
* The Identifier Name of the Status Effect you want to clone from

`StatusIdentifier` (string) <b>[REQUIRED]</b>
* Determines the Status Effect your template will be applied to, or the new Identifier Name of your custom status.
* Set to an existing Identifier to apply to an existing Status, or create a new one to create a new Status.

`NewStatusID` (integer) <b>[REQUIRED]</b>
* Sets the Preset ID of the Status Effect. This isn't really used by many things, but you should still set it.
* If you set to 0 or below, SideLoader will ignore this value completely.

`Name` (string)
* The name of your Status Effect. Unity rich text supported.

`Description` (string)
* Your status description.
* Status Effects can make use of special formatting to display the values of the effects.
* For example, typing `[E1V1]` in your effect description will be substituted to the "first value" from the "first effect" on the status. This may not always work depending on the actual effects you use.

`Lifespan` (float)
* The length of the Status Effect in seconds.

`RefreshRate` (float)
* How frequently the status effects are applied, in seconds.
* Depending on the effect, this may not matter. Most important for regeneration and DoT effects.

`BuildupRecoverySpeed` (float)
* How quickly the status buildup falls down to 0.
* Value is how much buildup falls per second.

`AmplifiedStatusIdentifier` (string)
* Determines the Status Effect which will be received if the player has Shamanic Resonance
* Set this to the Identifier Name of the Status Effect you want to set.
* Note: if you're setting this to a custom Status, you should set that one up first. SideLoader applies templates in alphabetical order (of the file name), so use that to apply the other one first.

`IgnoreBuildupIfApplied` (true / false)
* If false, buildup cannot be added when already 100 or if status is active.

`DisplayedInHUD` (true / false)
* Is the status visible in HUD?

`IsHidden` (true / false)
* Is the status completely hidden?

`IsMalusEffect` (true/false)
* Determines the category this effect is shown under in the HUD.
* `true` will show this effect in the Negative category, `false` will show it in the Positive category.

`Tags` (list of string)
* The `Tags` is a list of string (text) values. For statuses, these are not used that much.
* See [this Google Sheet](https://docs.google.com/spreadsheets/d/1btxPTmgeRqjhqC5dwpPXWd49-_tX_OVLN1Uvwv525K4/edit#gid=1840819680) for a list of tags.
* Do not include the tag number.

Your tags XML should look like this, for example:
```xml
<Tags>
  <string>Boon</string>
  <string>Status Type</string>
</Tags>
```

`EffectBehaviour` (enum)
* Relates to the <b>Effects</b> on your status.
* Explained on the Effects page.

`Effects` (list of `SL_EffectTransform`)
* See the [Effects](Effects/EffectTransforms) page for documentation on all SL_Effect classes, and more details on how to set up EffectTransforms.

## SL_ImbueEffect

Imbues are similar to Status Effects, but much simpler overall.

`TargetStatusID` (integer)
* The ID of the Imbue you want to clone from

`NewStatusID` (integer)
* The ID of the Imbue you want to apply to. Can be a new or existing ID.

`Name` (string)
* The name of your Imbue. Unity rich text supported.

`Description` (string)
* Your imbue description.

`EffectBehaviour` (enum)
* Relates to the <b>Effects</b> on your imbue.
* Explained on the Effects page.

`Effects` (list of `SL_EffectTransform`)
* See the [Effects](Effects/EffectTransforms) page for documentation on all SL_Effect classes, and more details on how to set up EffectTransforms.