# Conventions

"Conventions" refer to the practices, techniques, and styles that the maintainers enforce in contributions. Following conventions keeps the
codebase consistent, but why is consistency desirable? Consistency, for its own sake, is unimportant and can be actively harmful;
consistency to aid the intelligibility and maintainability of code is important because intelligibility and maintainability are important.
This document will describe conventions we have established as a reference for contributors to follow and for maintainers to refer to when
asking for changes from contributors.

# When to edit upstream vs. new _Moff files

The general rule is that all changes should be moved to a `_Moffstation` namespaced file; however, since this is impossible to do for 
edits to existing code, modifications can be made to upstream files where edits cannot be moved to a `_Moffstation` namespace.

Of course, all of this is subject to the contribution guidelines' directions on when to use `Moffstation` guards as well.

#### YAML

Entirely new prototypes should be put into a file somewhere under `Resources/Prototypes/_Moffstation/`.

Purely additive edits to existing prototypes should be made to the upstream file.

Mixed additive and removing edits can be made to the upstream file if the amount of YAML removed from the upstream definition is small. If
the amount of removed YAML gets too large, it is better to copy the prototype into the `_Moffstation` namespace and make the changes there,
leaving the old upstream entity in place with a small change to its ID indicating that it's the upstream version.

#### C#

Similar to YAML, new code should be put into a file somewhere under a `Moffstation/` namespace, and small changes to existing code can be made
to the upstream file.

#### RSIs

Upstream RSIs should almost never be edited. In any case where you might want to edit an upstream RSI, instead define a new RSI in the
`_Moffstation` namespace and update the usage of the RSI in YAML to use the new RSI. Merging changes to JSON is torture. Merging changes
to PNGs is impossible.

# Field order in YAML Entity Prototypes

Because prototypes are just YAML maps, the order of fields is not technically important, and your YAML will work in whatever crazy order
imaginable. However, to keep the YAML readable, fields should be in the following order:
- `type`
- `parents` / `parent`
- `id`
- `abstract`
- `localizationId`
  - Rare
- `name`
- `suffix`
- `categories`
- `placement` / `save` / `loc`
  - These are all rare, so it doesn't really matter what order they're in
- `description`
- `components`

# C# Conventions

#### Formatting
New code should use the Rider automatic formatter to enforce consistent formatting. Formatting-only changes to upstream code will be
rejected.

When breaking lines, the author prefers to break function invocations and similar constructs in the following way:

```csharp
myFunction(
    argument1,
    argument2
);
```

as opposed to
```csharp
myFunction(argument1,
    argument2)
```

because the arguments are at parallel levels of indentation. The author curses whoever thought the second approach was the right.

#### Warnings

All warnings in new code should be treated as errors. If the compiler or an anlyzer complains about something, that warning was probably
written by somebody who knows better than any of us, and so it should be resolved. In the cases where a warning is legitimately incorrect,
a `#pragma` or other suppression mechanism may be used, but it must be accompanied by a comment to justify its use.