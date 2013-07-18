# What is this?

This is a customized configuration for [KeyRemap4MacBook](https://pqrs.org/macosx/keyremap4macbook/) to make a keyboard home row to behave like Douglas Engelbart's [chord](http://en.wikipedia.org/wiki/Chorded_keyboard) device but only for "difficult to reach but very useful" keys

Unfortunately this only work in OSX, but if you are like me who works in a Linux virtual machines hosted by OSX then you can have the best of both worlds. 


# Why?

* My development environment is made of vim, zsh, tmux, i3 (tiled window manager), let's say that I *need* a lot of keybindings, avoid clashes with _"only"_ two modifiers (CONTROL and ALT) is not easy
* I'm not getting younger, twisting my hand and my wrist all day long to reach those modifier keys was causing me some cronic pain
* Being able to stay more in the home row is the ultimate keyboard efficiency goal


# How it works?

When you simultaneously press two keys they will be mapped to another (convinient) key. Al the mappings are simmetric, resolving another issue that many keyboards have

* D+F to CONTROL\_L
* J+K to CONTROL\_R
* S+D to OPTION\_L aka ALT\_L
* K+L to OPTION\_R aka ALT\_R
* E+F to ESCAPE
* J+I to ESCAPE

Now, this is something but I wanted to go beyond, to go towards the mythical [Space Cated Keybord](http://en.wikipedia.org/wiki/Space-cadet_keyboard), I wanted to have all those modifiers keys... Unfortunately KeyRemap4MacBook doesn't support those key codes... Fortunately inside a Linux VM I can (with xmodmap) remap some strange/unused keys into those key codes... There we go, 

* S+F to KEYPAD\_1 and then with xmodmap to META\_L
* J+L to KEYPAD\_2 and then with xmodmap to META\_R
* A+F to KEYPAD\_3 and then with xmodmap to SUPER\_L
* J+; to KEYPAD\_4 and then with xmodmap to SUPER\_R

I considered to add also HYPER\_L and HYPER\_R but for now I'm happy like that


# How to use it

* Install KeyRemap4MacBook
* Go to "Preferences" > "Misc & Uninstall" > "Open private.xml"
* Replace the default private.xml file with the one you find in this repository
* Go to "Change Key"
* Hit "Reload XML"
* A section called "Engelbart" should be appeared
* Enable all the mappings inside of it
* Enjoy :-)
