# Blend Swap Internationalization Project

Internationalization files for the Blend Swap website, community built.

We need help with 

* Portuguese
* More languages? mainly left-to-right written langs.

We're covered in __Spanish__, __German__, __Polish__, __French__, __Serbian__, __Greek__, __Portuguese__.

## Set up

### Requirements

* You will need a Github account and a basic knowledge of how to use Git for version control.
* [Fork](https://help.github.com/articles/fork-a-repo) this project. and __Watch__ it (top buton &uarr;) to get all updates from poifox.
* Download and install [PoEdit](http://www.poedit.net)
* Clone the full source files to your computer (you must [setup your ssh keys](https://help.github.com/articles/generating-ssh-keys) on Github for cloning and pushing code).

### Translating
* Let's say you will work with *YourLanguage*. In the sources root you will make this folder structure `lang/LC_MESSAGES` (if it doesn't exist already). The name of the `lang` folder is given by the three-character language codes in [ISO639-2 Standard](http://www.loc.gov/standards/iso639-2/php/code_list.php). The *LC_MESSAGES* subdir MUST HAVE THAT NAME. Take the Spanish translation as an example of the file structure.
* Open PoEdit for the first time it and enter your name and email when asked to. This is to keep a backlog of who commits what translations.
* From the PoEdit menu select __File > New Catalog from POT file__. Browse for the `default.pot` file in the sources root folder and open it.
* You will be promted for the information of the translation.
    Enter the following (bold is mandatory):
    * Project name and version: __Blend Swap Translation 0.1__
    * Team: __Blend Swap Translators__
    * Team's email address: __your@email__
    * Language: __YourLanguage__
    * Country: __Your Country Name__
    * Charset: __UTF-8__
    * Source code charset: __utf-8__
    * Plural forms: __nplurals=2; plural=n == 1 ? 0 : 1;__
* Hit *Accept*. The *YourLanguage* catalog is created. You will be prompted for where to save it:
* Save the file to the folder you created before as `default.po` (watch out for the extension, POT files are templates, PO files are translations files).
* Work on your translations and save frequently. __You can use any UTF-8 compliant alphabet; UTF-8 includes [practically all character sets known to mankind](http://en.wikipedia.org/wiki/List_of_Unicode_Characters).__
* When you're done do your normal `git add .` , `git commit -m "Commit message"` and `git push` to update your fork.
* When you feel your translation is ready, First check if your fork has a pull request from the main fork and merge it first. Next, check if the main is ahead of your fork, if so open a pull rquest from the main to your fork and merge it, THEN you can do a pull request from your fork to the main fork (poifox/blendswap-i18n) so we know you're ready for merge.
* __Do not use other software than poedit to edit the po files as it is very easy to break them, use PoEdit every time.__
* All this applies for `model_validation.po`, which should be put into `lang/LC_MESSAGES/model_validation.po`

### What NOT to translate:

* the word Blend, use your language's plural forms if you like, but keep it as blend, as not everything is a single type of asset (eg. ITALIAN: blend &amp blendi <= that's ok with us.).
* `%s`, `%d`, etc. These are placeholders for things that are replaced on runtime. put them where they make sense.

### New strings.

From time to time new strings will be added to the translation files. When this is the case our commits will say so. when you see new strings have been pushed up the server do the following:

* Synchronize your master branch with our master by opening a __[pull request](https://help.github.com/articles/using-pull-requests)__ from the main fork to yours; and merging it yourself.
* Open `lang/LC_MESSAGES/default.po` file with PoEdit and from the app menu select: __Catalog > Update from POT file__, browse for the `default.pot` file in the source root and accept it.
* The new strings will be listed. Hit accept to update the *YourLanguage* `default.po` file.
* Depending on your PoEdit settings some strings may be translated automatically; they appear yellowish, __YOU MUST ALWAYS DOUBLE CHECK THESE STRINGS BECAUSE YOU CAN NOT TRUST THOSE AUTOMATIC TRANSLATIONS__.
* Go back to translating as usual.

### Notes.

* The entire workflow applies to `default.pot` and `model_validation.pot`, which should be always be translated; the other `cake*.pot` files can be ignored.
* __DO NOT__ edit other files not pertinent to your language. the pot files in the root, the README and everything else that's not yours you should never EVER touch.
* We plan to update contributed translations at least once a week. Translating all these string doesn't take that long and it can be all done in a quick afternoon.
* PROTIP: when translating in PoEdit click on the first string, translate it and hit [ CTRL + DOWN ARROW ] the next string will be selected and you can type right away. This way you won't get tired of alternating between the mouse and the keyboard.
* The repository is setup to ignore the .mo files created by PoEdit, because they are binary data and bloat the commits. We compile them on the server so don't worry about them ;)
* __Do not use other software than poedit to edit the po files as it is very easy to break them, use PoEdit every time.__
