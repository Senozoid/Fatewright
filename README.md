# Fatewright
Fatewright is an opensoure project (written in Java) to facilitate the creation of custom text-based games, such as CYOA books, gamebooks or other kinds of interactive fiction books.

## Overview
### How it works
Fatewright relies on a concept of pages and a player character. A page is a text file with a .fwpg extension which contains the story text, along with some very simple scripts to tell the engine what to do when. For example, the player may be shown a certain passage from the page only if the player character passes a skillcheck, or if they have a certain item in their possession, and so on. You don't need to know any coding to write the scripts, see the [manual]() for more info. Other than the page files, Fatewright needs a player character, which is another text file, but with .fwpc extension, which may (but does not have to) contain separate sections for identity, stats and inventory. All of these are optional, and may remain unused, depending on the kind of game the author wants to create. Since .fwpg and .fwpc are text files, they can be potentially read or edited manually by the player, which may be undesirable. This is why, the author may choose to use the [cipher]() argument in the commandline. However, this is not foolproof because Fatewright is opensource. This is meant more as a deterrent for potential cheaters because it would be more fun to just play the game than to decipher it manually. But of course, an author may also choose to modify the code to their liking for the purposes of protecting the game information from manual viewing or editing.
### Is it for you
### 

## Other information
### Quick backstory (for my first GitHub repository)
When I was in college, I started making a text adventure game called Zenerian Chronicles. There were tools to help with this, but since at that time I was not aware of any such tools which gave me complete control over the game mechanics, I decided to build the game from scratch using my very limited Java knowledge. As I was writing the code for what would basically be the engine for my game, I realised that to give myself some freedom in the future, I was making the engine entirely independent of the story I write. This meant that others could use my engine to turn their own stories into interactive text games. And thus, Fatewright was born.
