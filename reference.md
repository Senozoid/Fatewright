# Contents

- [Designing](#designing)
- [Writing](#writing)
- [Publishing](#publishing)

# Designing

# Writing

In Fatewright, pages are the smallest coherent units through which the story is presented to the player. Each choice the player makes in the story, leads them to another page. These pages have story content, instructions for Fatewright, and finally, information about the options to be presented to the player. Pages are created through files with the extension ".fwpg", which stands for Fatewright page.

## Story text

### Comments

#### Line comments

Line comments begin with `//`, and are recognised only if not immediately preceded by a non-whitespace character.

```fatewright
This is visible text.//This will NOT be recognised as comment
This is visible text. //This WILL be recognised as comment
```

Once a line comment is encountered, the entire rest of the line (including the line break) is skipped by Fatewright.

```fatewright
This is line 1. //This is a line comment
This is still line 1.
```

#### Block comments

Block comments begin with `/*` and end with `*/`, and are recognised only if not immediately preceded by a non-whitespace character.

```fatewright
This is visible text./*This will NOT be recognised as comment*/
This is visible text. /*This WILL be recognised as comment*/
```

Block comments must not be immediately followed by a non-whitespace character either. Otherwise, Fatewright cannot recognise the end of the comment.

```fatewright
/*This is a comment that ends properly*/ This is visible text.
/*This comment never ends */because the ending sequence is not parsed properly.
```

If a block comment is followed by a line break, the line break is not ignored because it is not considered a part of the comment.

```fatewright
This is line 1. /*This is a block comment*/
This is line 2.
```

## Instructions

### Conditionals

```fatewright
$> BIO: !elf
$> BIO: human
"Finally, a fellow human," the woman said, shedding her annoyed expression.
$<
$!>
"I could use some help over here," the woman said, looking thoroughly annoyed.
$<
$> STAT: appearance>2 && combatskill>5
"And you look like you may be able to handle yourself as well," she added approvingly, measuring you with an experienced eye, "With these little ones, you might end up needing to."
$<

"Urghh, $case:gender he/she/this one/- smells even worse. Prithee, do not breathe on me," one of the children remarked, taking a step back from you. Then, turning to the woman, added, "Could you perhaps continue your conversation outside?"

The woman rolled her eyes and asked you, "Do you speak spoilt? Can you convince these brats that I am only trying to help them?"
$<
```

### Other commands

#### Quick cases

#### Flagging

#### Inventory management

### Escape character

# Publishing

## Compiling

## Packaging

## Releasing
