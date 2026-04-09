Figurine Guidelines
===================

In Moffstation, players are able to create a figurine for their characters. These figurines can be spawned randomly, and by opening moff figurine packs.

You can ask around on the discord if you would like someone to make your figurine for you.

### What you'll need to make a figurine

- **Your figurine name.** Written from the perspective of someone who doesn't know your character
:white_check_mark: slime Chief Engineer figurine
:white_check_mark: green lizard bartender figurine
:white_check_mark: tall janitor figurine
:x: Tania Buttersworth figurine
:x: extremely cool lizard figurine
:x: that guy's figurine

- **Your figurine description.** Again, written from the perspective of someone who doesn't know your character. Should start with "A figurine depicting..."
:white_check_mark: "A figurine depicting a pink slime chief engineer, with numerous tentacles and a tiny fire axe."
:white_check_mark: "A figurine depicting a lizard. They look like a goober."
:white_check_mark: "A figurine depicting a dishevelled catgirl."
:x: "Some guy idk"
:x: "They look like a guy you know"
:x: "A figurine of Tania Buttersworth in her engineering uniform"

- **Your figurine voice lines.** Anywhere from 3-5 iconic or common statements, such as a passing greeting, a catchphrase, something they often say on the job or a throwback to a round they remember well.
  - Voice lines can contain identifiers, like a characters name.
  - Voice lines should be written without an accent, if an accent is added it should be done via the accent component in post.
  - Voice lines should be written with proper grammar and spelling, unless doing otherwise is an explicit feature of the character.
  - Voice lines should not have excessive punctuation, no more than 2 "!" at the end of a sentence. They're figurines with tiny piezoelectrics, not loudspeakers.

- **A sprite with of approximately the same size.** Usually, we want all figurines to be about the same size. All texture files are 32x32, but are not completely filled out. You can use this one for reference:
<img src="../assets/gigsFigure.png" width=128 tyle="margin-left:auto;margin-right:auto;display:block;"/>

## Contributing
All relevant IDs should be written using the character's given name, not the name of the figurine. This is usually just their first name, or whatever you'd normally scream over comms for their attention (e.g. "Tania" for Tania Buttersworth, "Gigs" for Works-Many-Gigs, "Polly" for Pollyari)

Ensure all figurines are kept in alphabetical order when editing their relevant files. This helps keep them organised and makes it easier to find a relevant figurine easily.

- The YAML for the figurine prototype goes in `/Resources/Prototypes/_Moffstation/Entities/Objects/Fun/figurines.yml`
  - The prototype defines the figurine in game as an item.
  - Figurine prototypes parent off of the `BaseFigurineMoff` abstract prototype.
  - If the figurine has an accent, make sure to add the relevant component for that accent here.

- The voice lines for figurines goes in `/Resources/Locale/en-US/_Moffstation/datasets/figurines.ftl`
  - The fluent file contains all the voice lines a figurine can use.

- The YAML for the voice line dataset go in `/Resources/Prototypes/_Moffstation/Datasets/figurines.yml`
  - The dataset links the voice lines in the FTL file to a dataset that the figurine can use.

- The textures go in `Resources/Textures/_Moffstation/Objects/Fun/figurines.rsi`, and the `meta.json` file contained within should be updated as well
  - The RSI folder contains all the textures used by figurines. The meta.json file describes what all of the textures are for the game to use.

- The `id` for the figurine should be added to `MoffFigurineTable` in `/Resources/Prototypes/_Moffstation/Entities/Markers/Spawners/Random/toy.yml` 
  - The figurine table is used by the game to spawn in moff figurines in figurine boxes and random figurine spawners.