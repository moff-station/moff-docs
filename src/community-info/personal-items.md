Personal Item Guidelines
========================

In Moffstation, players are able to create a cosmetic personal item for their characters.
This is meant to be a fun way to express your character's personality, style, or story.

Personal items are limited to one per character.

## Guidelines
- Personal items cannot be weapons, tools, protective gear, or provide any mechanical advantage at round start.
  - This restriction is overridden if the item is a reskin of round-start job equipment; however it must remain mechanically identical and be restricted to that job.
- Personal items cannot visually conflict with other roles or include special visual effects.
- Personal items should include a brief 1–2 sentence in-character description, with additional details placed under a `DetailExaminable` component.
- Personal items cannot be contraband, fall into grey-area legality, or otherwise create issues for security.


### Examples
- **Allowed**: A small, black, leather notebook with a red ribbon bookmark. It is writable, or it can have papers stored inside it, similar to a folder.
- **Allowed**: A small pendant with a picture of a cat on it. It can be opened or closed using a `ToggleItem` interaction.
- **Allowed**: A keychain that has a small miniature AI core on it. The sprite flashes with activity, and it can be turned on and off using a `ToggleItem` interaction. The AI core is not inhabitable by any ghost or player.
- **Allowed**: Any custom instrument (not a Digital Audio Workstation or similar).
  - This is **disallowed** if it is a reskinned instrument that has any extra functionality or bypasses checks, like not requiring you to have it in your primary hand, unless that behavior is default.
- **Allowed**: Any custom plushie normally available in-game.
- **Allowed**: Any toy that is normally available in-game.
- **Allowed**: Mantles for your character that fit the style or color theme of your character.
  - This is **disallowed** if it looks like a higher rank or command mantle.
- **Disallowed**: A reskinned pen parented off of the Cybersun pen, which can be used as a screwdriver, does damage, has a contraband status, and can rewrite papers.
- **Disallowed**: A syndicate scarf. This is normally an illegal item.


### Job-related Items

Personal items mimicking a job-related item should be parented to the item you want to mimic.
This is done to ensure that the item behaves like the original item, and does not have any extra functionality.

This also makes upstream item balancing trickle down to functional personal items,
so items don't have to be manually re-balanced.

## PR Guidelines
When creating your personal items, be sure to follow the following guidelines.

Personal items content goes in the `_Moffstation` namespace under a `PersonalItems` folder. The item should be sectioned based on the type of item. For example:
   - If the item is a pen, it should be in `_Moffstation/PersonalItems/Items/...`
   - If the item is primarily a worn cosmetic, it should be in `_Moffstation/PersonalItems/Wearables/...`

Personal item content is organized in this structure. Be sure to separate textures and the item YAML like so:

- `Resources/Textures/_Moffstation/PersonalItems/Items/(playername)/(charactername)/ItemName.rsi` (the item RSI folder)
- `Resources/Prototypes/_Moffstation/PersonalItems/Items/(playername)/(charactername)/ItemName.yml` (the item YAML)

For example:
- `Resources/Textures/_Moffstation/PersonalItems/Wearables/FrostWinters/Frost_Winters/frostmedicalwebbing.rsi` (the item RSI folder)
- `Resources/Prototypes/_Moffstation/PersonalItems/Wearables/FrostWinters/Frost_Winters/frostmedicalwebbing.yml` (the item YAML)

When writing YAML for your item, write the prototype for your item first, and then the custom loadout group for your item.

The beginning of the YAML should state the player username and the character name. For example:

```yaml
# Player FrostWinters - Character: Frost Winters

- type: entity
  parent: ClothingBeltMedicalFilled
  id: PersonalItemFrostMedicalWebbing
  name: "Winters' medical rig"
  description: "Winters' chest rig brought from home, modified to fit medical supplies. Looks oddly familiar to some with certain backgrounds."
  suffix: PersonalItem, Filled
  components:
  - type: Sprite
    sprite: _Moffstation/PersonalItems/Wearables/frostmedicalwebbing.rsi
  - type: Clothing
    sprite: _Moffstation/PersonalItems/Wearables/frostmedicalwebbing.rsi

- type: loadout
  id: PersonalItemFrostMedicalWebbing
  equipment:
    belt: PersonalItemFrostMedicalWebbing
  effects:
  - !type:PersonalItemLoadoutEffect
    character:
    - Frost Winters
```

Lastly, add the `id` of the item to `_Moffstation/PersonalItems/personal_loadout_groups.yml`, make sure its inserted in alphabetical order.

### Shared Personal Items
If you want to create a personal item shared between multiple characters (including characters that are not yours),
you can create a shared personal item.

If the item is shared between multiple characters which all belong to you (you play these characters),
it should be in the `_Moffstation/PersonalItems/Wearables/(playername)/Shared` folder.

If the item is shared between multiple characters, and some of those characters do not belong to you (you do not play some of these characters)
it should be in the `_Moffstation/PersonalItems/Wearables/Shared` folder.

Shared personal items count as one personal item for each character that uses it.

## Approval
Personal items are subject to approval by any Moffstation maintainer or admin. Personal item guidelines are guidelines, not explicitly rules, so if you're unclear if your item would be allowed, please ask a maintainer or admin for clarification.