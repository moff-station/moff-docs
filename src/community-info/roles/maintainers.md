# Moffstation Maintainers

## Responsibilities

Firstly, the everpresent caveat: all members of Moffstation staff are volunteers with no requirement to do anything.
That being said, maintainers maintain the technical product that is Moffstation involving input and care across
various areas.

#### Pull Request Reviews

Perhaps the largest responsibility of the maintainer is to be the gatekeeper of changes to the codebase. Maintainers
have merge permission to the repo, and so can merge their own and others' PRs. Along with this privilege, maintainers
have the responsibility to review and enforce quality of contributions. Maintainers should focus on three facets of any
change request:
- Functional content:
  - Is this a good addition to Moffstation?
  - Does this fit into our design pillars?
  - Is this balanced?
  - Does the player base want this?
- Technical correctness:
  - Is this the right way to implement this?
  - Does this changeset use best practices and modern techniques?
  - Is this changeset's complexity maintainable going forward?
  - Will we need to change this in the future, and if so, is it worth it?
- Correctness of contribution requirements:
  - Does this use namespacing / guards correctly?
  - Is the PR template adequately filled out?
  - Is the changelog correct and useful?

When maintainers agree on the questions they should ask, they can agree on what is important when considering contributions
to the codebase. By asking these questions and demanding good answers, the quality of the codebase is maintained.

#### Keeping up with Upstream

As of writing, Moffstation is a soft fork of Wizard's Den. This means we pull down most of what Wizard's Den does while tweaking
some things like balance, and while adding or removing some other things which do not align with our design pillars or player
desires. To keep this up, a maintainer must `git merge` changes from Wizard's Den regularly. In theory, anyone can do this, but
we require its performed by a maintainer as it's technically involved and the resulting PRs are virtually unreviewable,
so they necessitate some trust to merge.

#### Maintaining Build Stability

Space Station 14 has a suite of automated tests and other checks which run on every PR to validate that the game remains playable.
Sometimes, issues arise either from upstream or from our own contributions which cause these checks (or even players' clients!) to
become unstable. This, at best, slows down development of contributions and, at worse, means players can't play on Moffstation at
all. Maintainers investigate, diagnose and fix these issues to ensure contributions continue to flow and players continue to play.

#### Player Issue Triage

It turns out Space Station 14 is not the most polished game. Players will find issues, and it falls on maintainers to fix these issues.
Maintainers should review bug reports to determine if they are an upstream issue or a bug in Moffstation, and if it is a bug in Moffstation,
maintainers should log it as a GitHub issue and/or fix it. Ideally, contributors fix issues with their own contributions, but it falls on
maintainers to more immediately resolve issues which require speedy resolution. Sometimes the best resolution is a judicious reversion of a
buggy contribution.

#### Being the Model Contributor

On top of all of those boring responsibilities, maintainers are the first-among-equals of contributors. As with all other contributions,
maintainers' contributions need to follow all rules, pass all checks, and meet all quality requirements like any other contributions.
However, maintainers' should act as examples to other contributors on how to write PRs and act in reviews.

#### Team Membership & Communication

Moffstation is, again, a collaboration between various volunteers who want to have fun playing and enhancing the game we all care about.
To this end, maintainers are part of the Moffstation Staff team where we respect each other as individuals and peers. Any staff members,
including maintainers, must be civil, able to communicate constructively, and act with respect and good-faith towards each other and the
entire Moffstation community. This extends from the Discord to reviews on PRs and, to a lesser extent, anything which can impact
Moffstation's reputation within the broader SS14 community.

### Anti-responsibilities

Maintainers are not / do not do:
- They are not admins. They have no power to resolve in-round issues. Maintainers do not get any in-game admin powers.
- Hosting infrastructure maintainers. Because of exactly how Moffstation hosting works right now, the closest maintainers get to this is
  publishing changes to the Moff CDN. The actual server hosting, CDN hosting, etc. is handled by the project owner.
- Have any Discord moderation powers. Moffstation the SS14 server and Moffstation the Discord server are basically the same thing, but
  maintainers only have power over the SS14 server. The one slight caveat is that maintainers have pinning power in their related discord
  channels.

### Domains

Maintaining Moffstation requires various disparate skills which are rarely all present in any one individual. Thus, different maintainers
deal with different domains in which they have necessary experience. The domains include:
- YAML: the low-code layer which defines the bulk of SS14's content. Relatively easy to get into.
- C#: what the game is actually implemented in. I hope you know what a type system does.
  - This includes automated tests and upstream merges
  - If a maintainer can deal with C#, they must also deal with YAML
- Art: while it is a different skillset from coding, maintaining Moffstation's visuals is no easier or less valuable
  - Ideally, art maintainers should know some more technical SS14 specific details like displacement maps, how sprite specifies work, etc.
- Mapping: authoring maps is "YAML", but so much larger in scale and detail that it requires a different skillset.
  - Mapping maintainers should have a good understanding of what players want in maps and also should know what makes for an interesting map.
- Meta work: `@peers through the fourth wall, making eye contact with the reader.`
  - Maintainers need to maintain things which don't go into Moffstation, the game, like documentation of goals, processes, or designs.

## Hierarchy

As of writing, maintainers have no hierarchical organization. The project lead is the de facto lead maintainer and everyone else is equal.
If disagreement comes up, maintainers offer their opinions, and those opinions are weighed by the experience in the relevant domain, but
ultimately disagreement is settled by the project lead's decision.

## How to become one

Firstly, because maintainers are given access to privileges which can obliterate the repository, a maintainer candidate must be a trusted
member of the Moffstation community. Secondly, a maintainer candidate must show capability in the skills and responsibilities described
above. Not all maintainers will check all boxes, but a candidate needs to demonstrate enough prospective value to be worth considering.

If those two qualities exist in one person, that person can ask to be considered for a maintainer position. Right now, there's no process and
we've taken on maintainers as they have shown interest. The best way to be considered is to ask a current maintainer or the project owner,
at which point the existing maintainers will convene and decide. If they agree, congratulations, you're a maintainer now; just hang on while
the project lead provisions your access.