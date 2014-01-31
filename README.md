# What is this?

This is a customized configuration for [KeyRemap4MacBook](https://pqrs.org/macosx/keyremap4macbook/) to make a keyboard home row to behave like Douglas Engelbart's [chord](http://en.wikipedia.org/wiki/Chorded_keyboard) device but only for "difficult to reach but very useful" keys

Unfortunately this only work in OSX, but if you are like me who works in Linux virtual machines hosted by OSX then you can have the best of both worlds. 


# Why?

* My development environment is made of vim, zsh, tmux and i3 (tiled window manager), let's say that I *need* a lot of keybindings, avoiding clashes with _"only"_ two modifiers (CONTROL and ALT) is not easy
* I'm not getting younger, twisting my hand and my wrist all day long to reach those modifier keys was causing me some pain
* Being able to stay more in the home row is the ultimate keyboard efficiency goal


# How it works?

When you simultaneously press two keys they will be mapped to another (convinient) key. Al the mappings are simmetric (this resolves another issue that many keyboards have)

* D+F to CONTROL\_L
* J+K to CONTROL\_R
* S+D to OPTION\_L aka ALT\_L
* K+L to OPTION\_R aka ALT\_R
* E+F to ESCAPE
* J+I to ESCAPE
* E+R to BACKSLASH aka vim's LEADER
* U+I to BACKSLASH aka vim's LEADER
* W+F to CONTROL\_L + OPTION\_L
* J+O to CONTROL\_R + OPTION\_R
* Q+F to CONTROL\_L + SHIFT\_L
* J+P to CONTROL\_R + SHIFT\_R

Now, this is already something, but I wanted to go beyond, towards the mythical [Space Cadet Keyboard](http://en.wikipedia.org/wiki/Space-cadet_keyboard), I wanted to have all those modifier keys... Unfortunately KeyRemap4MacBook doesn't support those key codes... Fortunately inside a Linux VM I can (with xmodmap) remap some strange/unused keys into those key codes... There we go

* S+F to KEYPAD\_1 and then via xmodmap to META\_L
* J+L to KEYPAD\_2 and then via xmodmap to META\_R
* A+F to KEYPAD\_3 and then via xmodmap to SUPER\_L
* J+; to KEYPAD\_4 and then via xmodmap to SUPER\_R

In the future I will consider to add also HYPER\_L and HYPER\_R but for now I'm happy like that


# How to use it

* Install KeyRemap4MacBook
* Go to "Preferences" > "Misc & Uninstall" > "Open private.xml"
* Replace the default private.xml file with the one you find in this repository
* Go to "Change Key"
* Hit "Reload XML"
* A section called "Engelbart" should appear
* Enable all the mappings inside of it
* Enjoy :-)


# Last tip

With [PCKeyboardHack](https://pqrs.org/macosx/keyremap4macbook/pckeyboardhack.html.en) I've remapped my CapsLock to Fn key, so that I can have yet another (sort of) modifier key in my home row! What I do with Fn? With KeyRemap4MacBook I've remapped Fn+{H,J,K,L} to... I'll let you guess what :-)
