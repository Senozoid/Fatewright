# Quick Guide to Fatewright (INCOMPLETE)
## Format of the pages (.fwpg files)
### Overview
Pages, or pagefiles, are the smallest coherent units through which the story is presented to the player. Each choice the player makes in the story, leads the program to another page. These pages have story content, instructions for Fatewright, and finally, information about the options to be presented to the player. Page files have the extension ".fwpg", which stands for Fatewright page.
### Scripts
Each page has two sections, separated by `/--`, the former being the main story content of the page. Within the story content may be runtime instructions for Fatewright, also known as scripts. Each instruction is triggered by a keyword, here referred to as a command. These commands are of three types: inline, invoked, and nestable. \
**Inline** commands are not really commands, more like single-word cues generally used for formatting (newlines, paragraphs etc), and can be used in the same line with the story text, hence the name. \
**Invoked** commands are less simple, and are preceeded by a `/` and a whitespace. The `/` declares that the next word is an invoked command. These commands expect arguments, and often (though not in all cases) parse the remainder of the line they appear in, to find them. This is why it is good practice to write each invoked command in its own separate line along with its arguments. \
**Nestable** commands are similar to invoked commands in that they expect arguments, but they are more complex (and more powerful) than invoked commands. Each nestable command opens its own reader (think sub-page), where other commands can appear just like they appear anywhere else in the page. Several levels of nested nestable commands can be written in this manner. However, since this uses recursion to achieve the nesting, it is advisable to use it sparingly. \
Nestable commands are invoked with a `/>` followed by a whitespace and the command, and are ended with a `/<` followed by a whitespace and the depth of the nest level which is to be closed. The top level is `0`, and it increases the deeper the nesting grows. \
This is an example:
```
/> race Human
"Oh, you're a human," she said, relief showing in her face.
/> gender Male
"Yes, but he's a man," the older woman said, looking you over cautiously.
/< 1
/> gender Female
"And a woman, thankfully," the older woman said, relaxing.
/< 1
"Either way," the younger one replied, "We don't have a choice."
/< 0
```
Apart from these commands, line comments as a part of the text are also supported. Everything in a line after `/!` is ignored by Fatewright, as long as it is not on the same line as an invoked or nestable command, or the closing of one. \
If the author wishes to use `/` as a word within the story content, it has to be instead written as `//`. This relies on the hope that `//` itself will not need to be used as a word in the story. \
The important thing to remember about the scripts, is that whitespaces and linebreaks are meaningful, and it is advisable to understand when to and when not to use them.
### Options
The only thing that appears in the section after `/--` is information about the options to be presented to the player. Not all options may be available to the player in all cases. Each group of options which are made available under the same set of conditions, is referred to as an opt group. The first mention of an opt group happens under a condition check in the script, before the `/--`. This is referred to as the declaration of the opt group.
