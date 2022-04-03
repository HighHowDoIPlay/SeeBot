# SeeBot
Fortnite: Save The World Discord bot.

This repository is meant to house all the Language files used in See-Bot.

You are welcome to contribute translations of the strings to improve See-Bot's (planned) Localization. If you plan on contributing to the project, please read the outline below.

## How-to-help
- Pick a language you're fluent in
- Download the **English** version of the files
- Translate the values to your desired language, preserving markdown and variables (See "[Formatting Help](#formatting-help)" below)
- Rename each file you translate to include the appropriate Language Code at the end of the file name, before the file extension (See "[Naming Help](#naming-help)" below)
- Make a pull request containing the updated Localization files.

## Formatting Help
So you've decided you want to translate a file, but you don't know what you should and shouldn't be changing.
Let's start by taking a look some examples:
```
KeyOne=This is a value with `markdown` and variables %arg0%.
KeyTwo=This is just a normal value.
#This is a comment.
```
Taking a look at the start of each line, you can see they start with a word (or phrase) followed by an equals sign. This is a `Key`. Everything after the equals sign is the `Value`. **DO NOT** modify `Key` names, or else See-Bot won't be able to find the `Value` associated with it anymore.

In `KeyOne`, it uses a mixture of [Discord Markdown](https://support.discord.com/hc/en-us/articles/210298617-Markdown-Text-101-Chat-Formatting-Bold-Italic-Underline-) and variables. The text `%arg0%` is a variable that gets replaced programatically by See-Bot, filling it in with a changing-value (example: A Fortnite Username, which is different for each user).
In `KeyTwo`, it has no markdown or variables, for comparison.

Other things to avoid removing/translating are unicode characters, line breaks, and other code escape sequences. Examples of these include `\u3242 \n \r \t \\`. Removing/translating these will break formatting or emojis that the bot uses.

Lines starting with `#` are comments, and do not get read by the bot. Do not modify comments. You are welcome to add your own comment in files you worked on (i.e: `#File edited by HighHowDoIPlay`). Don't claim others' work as your own.

When modifying a `.properties` file, it is recommended to use [Notepad++](https://notepad-plus-plus.org/downloads/) or a similar Rich-Text-Editor. This will help you easily distinguish between what is and isn't a key, and just provide an easier editing experience overall.

**NOTE**: Please be sure to check back here often, as I may the help information/"rules" on submitting.

You're also welcome to [Join the See-Bot Discord](https://discord.gg/F7musYd), where I'll be posting updates and etc about the project.

##Naming Help

You've downloaded the English Language files, have started to translate them but now you don't know what to save the file name as.

1. First, you'll want to open the [Java 8 Supported Locales](https://www.oracle.com/java/technologies/javase/java8locales.html) webpage.
2. Then, you'll want to find the Language you've decided to translate. We'll use `Spanish (es)`, specifically the Mexico version as an example.
3. Next, find the language tag (5th row). For our example, it's `es-MX`. This is what you'll be including in the file name, but you will need to make some modifications first.
4. Add a \_before the start of the tag, and replace the - with a \_ as well. Then, change any uppercase letters to lowercase. `es-MX` becomes `_es_mx` in the example.
5. Add your new language tag to any file you translate. For example, if you updated `CommonStrings.properties` to have Spanish translations for Mexico, you'd update the file name to `CommonStrings_es_mx.properties`.

If you still need assistance [Join the See-Bot Discord](https://discord.gg/F7musYd), and ask for help in the `#properties-help` channel.

## Missing Keys
If you see a "MissingKeys" error in See-Bot, it's due to one of the following:
1. I copy and pasted some code and forgot to change what file the Language Handler is pointing to.
2. The key is misnamed in the properties file.
3. The key is misnamed in the code.

If it's issue 1 or issue 3, it's best to contact me on the [See-Bot Discord](https://discord.gg/F7musYd) (above) and tell me what is broken.
If it's issue 2, then you should make a pull request with the fix before contacting me, or if you don't know how to do that, just contact me on the [See-Bot Discord](https://discord.gg/F7musYd).
