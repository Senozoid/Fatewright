# Fatewright (WORK IN PROGRESS)

## Links

+ [Reference](reference.md) _(WORK IN PROGRESS)_

## What is it?

Fatewright is an open-source system for writing choice-based text games. It is great for writing simple interactive stories, as well as for games with more complex logic. 

You do not need any special software to write an interactive Fatewright story; but to play it, you need a software that interprets stories written using this system. You can use the original interpreter provided here (which happens to share its name with the writing system), but you can also write your own if you know programming. Since this is an open-source project, you can also take this original code and modify it to suit your needs.

## Is it for you?

Fatewright was made because I wanted to write my own electronic gamebook. When I started it, I was not aware of the interactive fiction [communities](https://emshort.blog/how-to-play/the-if-community/) or any of the existing [systems](https://www.ifwiki.org/Authoring_system) like Inform, ChoiceScript or Twine. Later, I continued using my own system because I made it myself, was comfortable using it, and could change anything I did not like. If you are just starting out, you might find one of the more well-known systems to be better suited to your needs.

---

**If any of these apply to you, then Fatewright may be the tool for you :--**

+ You want to write a primarily choice-based story.

+ You do not care about having illustrations in your story.

+ _(NOT NECESSARY)_ You like to tinker with code, and may be familiar with Java.

**If any of these apply to you, then Fatewright is not what you want :--**

+ You want to create a game with music and illustrations.

+ You are looking for a tool to write a parser-based adventure.

+ You are looking for a tool to write a hyperlink-based browser game.

## How does it work?

Fatewright relies on a concept of "pages". These are units of storytelling; each player decision or turn of events leads to a new page in the story. The simplest of pages may contain a static block of text, followed by options that the player can choose from. Once the player has read the content of the page, they may choose one of the options, which determines the next page. And the story continues to progress until the player character meets their demise, or reaches one of the endings in the story.

It is perfectly fine to write a story comprised entirely of static blocks of text, but so much more is possible. If the author wants, they can write complex, nested condition checks in the page. For example, the player may be shown a certain passage from the page only if the player character passes a skillcheck, or a certain option may be available to the player only if they have a certain item in their possession, and so on. The author may also store values in variables to refer to later in the story. The options under the page may also be more fine-grained: an option to go through a portal that leads a wizard character to the correct page, may lead a bumbling fool someplace entirely different. Or, there may be two options that lead to the same page but change the story variables differently.

No real coding knowledge is required for any of this. However, if the author is familiar with Java, they can control every single detail about the mechanics of the game to have an extremely customised RPG.

For more detailed information to start writing your story, take a look at the [reference](reference.md) _(WORK IN PROGRESS)_.

## How to get started?

## How to contribute?

## Other info
