# Quick Guide to Fatewright
## Format of the pages (.fwpg files)
### Overview
Pages, or pagefiles, are the smallest coherent units through which the story is presented to the player. Each choice the player makes in the story, leads the program to another page. These pages have story content, instructions for Fatewright, and finally, information about the options to be presented to the player. Page files have the extension ".fwpg", which stands for Fatewright page.
### The script
Each page has two sections, separated by `/--`, which signifies the end of story content of this page and the beginning of option information. Within the story content may be runtime instructions for Fatewright. Each instrcution is triggered by a keyword, or command. These commands are of three types: inline, invoked, and nestable.
