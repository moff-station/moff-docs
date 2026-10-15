# This is a draft!!

- Content in < angle brackets \> is poorly worded should be replaced with well-edited prose.
- Sections that are bullet points now may be expanded into prose if the content would be better presented thusly.
- The standard by which I'm judging whether content should be in this doc or not is wether or not the content answers a question / resolves
  a discussion that's come up
  - eg. no chef digiboard because < point to the part of the doc where we say "no, service workers don't get microelectronics beyond their PDA" \>
    - throwback to forks where you didn't even get a freaking PDA (`cent-salivating-at-the-idea-of-taking-pdas-away-from-passengers.webp`)

<hr/>

# Game Feel

## Purpose

Where our [game design pillars](./design-pillars.md) inform what features off Moffstation should be and the art guide
informs how Moffstation should look, this document will describe how it should _feel_ to play Moffstation. This informs
how some features should be implemented, how aspects of the UI experience work and look, and generally how we would like players
to interact with the game.

< maybe define verisimilitude and how it applies here \>

## How the game should feel

- Interactions should be mechanically and visually immersive
  - Entity-bound user interfaces (ie. not the chat pane, context menus, etc.) should look like a real physical interface of the entity
    - the Access Configurator UI should look like a device used by a station security administrator
    - the RCD's radial UI should look like the configuration settings on an industrial device
  - Immersion should not be so deep as to be tedious
    - the RCD's radial UI is the right level of convenience to be useful without getting in the way
  - Examples:
    - [Still There](https://www.youtube.com/watch?v=733Fx_h8FIk)
    - The wires panel in SS14 today -- especially since you interact with it by holding specific things in your hands and interacting with
      particular UI elements! This is a great marriage of the UI with the game world!

- Judicious use of interactive friction
  - The right amount of friction can enhance immersion
    - eg. substation UIs -- double duty in both an immersive UI and in interacting with the device in an immersive way
      - substation "friction" is more like making a slightly suboptimal UX to permit immersive interaction and present immersive aesthetics
    - "Multiblock" machines like the PA, TEG, and -- to a lesser extent -- AME have more friction compared to just 1x1 machines, but their
      bulk makes them believable
  - Frequent interactions should be lower friction
    - The "chunky button" vending machine UIs are a great example of immersive UI/X, however as of October 2026, it involves a lot of
      clicks, especially if you want to vend the same thing multiple times. This is too much friction (rip botanists, chemists, etc.) and
      is a great candidate for QoL -- in this case in the form of enabling keyboard entry of selections.
  - Dealing with friction fills out job duties
    - The station's solar panel tracking is a great example -- takes time, thought, etc.
  - Frictionous interactions should be provided with the tools to overcome the friction
    - Solar panel tracking is a BAD example here. You can near-perfectly overcome the issue of setting up the tracker with some math and
      tracking of times, but the game doesn't give you the tools to do that time tracking.
    - A real solar tracker would come with the tools needed to overcome that issue -- this is verisimilitude.
  - Overcoming friction through skill is meaningful skill expression and is a good thing, even if it's overcome in a way other than we, the designers, intended
    - Caveat for cheese, we should always reserve the right to say "you're trivializing the mechanic in a way that's unhealthy"

- Core gameplay loops should not be made trivial
  - "Quality of life" improvements should be considered very carefully, lest we slip toward the [I Win Button](https://www.curseforge.com/minecraft/mc-mods/the-i-win-button)
  - < QoL slop is the enemy of game feel \>
  - Be careful not to conflate _trivial_ and _easy_. Some game loops should be easy.

- Immersion is informed by lore
  - Different factions have different UI aesthetics which prioritize different things
  - Different factions have different tools emphasizing different things

## Cassette Futurism

< Describe how cassette futurism informs UI/UX, device capabilities, etc. \>
