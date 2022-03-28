# SeeBot
Fortnite: Save The World Discord bot.

This repository is meant to house all the Language files used in See-Bot.

You are welcome to contribute translations of the strings to improve See-Bot's (planned) Localization. If you plan on contributing to the project, please read the outline below.

## How-to-help
- Pick a language you're fluent in
- Download the **English** version of the files
- Translate the values to your desired language, preserving markdown and variables (See "[Formatting Help](#formatting-help)" below)
- Make a pull request containing the updated Localization files.

## Formatting Help
So you've decided you want to translate a file, but you don't know what you should and shouldn't be changing.
Let's start by taking a look some examples:
```
KeyOne=This is a value with `markdown` and variables %arg0%.
KeyTwo=This is just a normal value.
```
Taking a look at the start of each line, you can see they start with a word (or phrase) followed by an equals sign. This is a `Key`. Everything after the equals sign is the `Value`. **DO NOT** modify `Key` names, or else See-Bot won't be able to find the `Value` associated with it anymore.

In `KeyOne`, it uses a mixture of [Discord Markdown](https://support.discord.com/hc/en-us/articles/210298617-Markdown-Text-101-Chat-Formatting-Bold-Italic-Underline-) and variables. The text `%arg0%` is a variable that gets replaced programatically by See-Bot, filling it in with a changing-value (example: A Fortnite Username, which is different for each user). In this context the `0` is referring to which value will be used (0 being the first value in the list), and the rest of it is just for See-Bot to know what to replace and where.
In `KeyTwo`, it has no markdown or variables, for comparison.

When modifying a `.properties` file, it is recommended to use [Notepad++](https://notepad-plus-plus.org/downloads/) or a similar Rich-Text-Editor. This will help you easily distinguish between what is and isn't a key, and just provide an easier editing experience overall.

**NOTE**: Please be sure to check back here often, as I may the help information/"rules" on submitting.

You're also welcome to [Join the See-Bot Discord](https://discord.gg/F7musYd), where I'll be posting updates and etc about the project.
