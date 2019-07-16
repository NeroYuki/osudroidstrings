<br>This repo stores the language files that osu!droid uses.
<br>You can contribute translation for osu!droid from here.

## Where to find the language files
All language files are in the folder [/osudroidresource/src/main/res](https://github.com/EdrowsLuo/osudroidstrings/tree/master/osudroidresource/src/main/res)
<br>The [values](https://github.com/EdrowsLuo/osudroidstrings/tree/master/osudroidresource/src/main/res/values) 
folder contains the English language files 
<br>The other folders are for other languages (e.g. values-zh is for Chinese)
<br>The available language locale codes are [here](https://stackoverflow.com/a/7989085) so if your language is not in the list, feel free to create a new folder name "value-<whatever locale code goes here>"

## How to make your first translation
For the most completed translation, you should use the default [values](https://github.com/EdrowsLuo/osudroidstrings/tree/master/osudroidresource/src/main/res/values) folder as reference, translate those files to your language and save them as new file with the same name in the desired folder
<br>in all values folder you will see a bunch of .xml file. Don't worry. These file are perfectly okay to be opened as a text file if you choose any text editor to open it
<br>It should look like this<br>
![How it should look like](https://i.ibb.co/sgTF351/cacac.png)
<br>(*I'm using visual studio code to open it, but feel free to open it with any text editor*)
<br>You will need to translate these file in ordered of priority
* options.xml (store every option text, the biggest one)
* strings.xml (store some in-game text)
* act_import_replay_res.xml and score_menu_fragment.xml are completely optional (their purpose is quite explainatory already)

<br>Alright, now i know some of you might be really confused by all this coding stuffs, but don't worry, we wont't have to learn that much
<br>First, let's tackle the main stuffs all the in-game text is store in this format, or similar
```xml
<string name="TEXT_NAME_GOES_HERE_DONT_TOUCH"> TEXT_VALUE_GOES_HERE_PLEASE_TRANSLATE </string>
}
```
<br> Basically, if it is between <...> and another <...> and not locate inside another <...>, please translate that text

## How to deal with all the confusing stuffs while translating
.xml file is encoded in Unicode so you can type whatever character you have in your translating language file, but you will face some rather nasty things that can cause format error for your language file
1. Escape character
<br>For example you want to translate something like *Don't*, *"Super" Slider*, *You're*, you will encouter `"` and `'` which in programming might cause some error if you use it without an **Escape Character** namely `\`, remember to put it before those `'` and `"`
