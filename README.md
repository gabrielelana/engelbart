# What is this?

This is a customized configuration for [KeyRemap4MacBook](https://pqrs.org/macosx/keyremap4macbook/) to make a keyboard home row to behave like Douglas Engelbart's [chord](http://en.wikipedia.org/wiki/Chorded_keyboard) device but only for "difficult to reach but very useful" keys

At least it's started this way... Later I started to use also the row above and below the home row, all keys far more reachable than the ones they replace

**NOTE:** Unfortunately this only work in OSX. If you are like me who works in Linux virtual machines hosted by OSX then you can have the best of both worlds.


# Why?

* My development environment is made of Vim, Zsh, Tmux and i3 (a tiled window manager), let's say that I *need* a lot of key bindings, avoiding clashes with _"only"_ two modifiers (CONTROL and ALT) is not easy
* I'm not getting younger, twisting my hand and my wrist all day long to reach those modifier keys was causing me some pain
* Being able to stay more in the home row is the ultimate keyboard efficiency goal


# How it works?

When you simultaneously press two keys they will be mapped to another (convenient) key. All the mappings are symmetric (this resolves another issue that many keyboards have)

* `D+F` to `CONTROL_L`
* `J+K` to `CONTROL_R`
* `S+D` to `OPTION_L` (aka `ALT_L` in Linux)
* `K+L` to `OPTION_R` (aka `ALT_R` in Linux)
* `E+F` to `ESCAPE`
* `J+I` to `ESCAPE`
* `W+F` to `DELETE`
* `J+O` to `DELETE`
* `E+R` to Vim's `LEADER`
* `U+I` to Vim's `LEADER`
* `C+V` to `CONTROL_L+OPTION_L`
* `M+,` to `CONTROL_R+OPTION_R`
* `X+V` to `CONTROL_L+SHIFT_L`
* `M+.` to `CONTROL_R+SHIFT_R`
* `X+C` to `OPTION_L+SHIFT_L`
* `,+.` to `OPTION_R+SHIFT_R`
* `Z+V` to `CONTROL_L+OPTION_L+SHIFT_L`
* `M+/` to `CONTROL_R+OPTION_R+SHIFT_R`

Now, this is already something, but I wanted to go beyond, towards the mythical [Space Cadet Keyboard](http://en.wikipedia.org/wiki/Space-cadet_keyboard), I wanted to have all those modifier keys... Unfortunately KeyRemap4MacBook doesn't support those key codes... Fortunately inside a Linux VM I can (with xmodmap) remap some strange/unused keys into those key codes... There we go
* `S+F` to `KEYPAD_1` and then via xmodmap to `META_L`
* `J+L` to `KEYPAD_2` and then via xmodmap to `META_R`
* `A+F` to `KEYPAD_3` and then via xmodmap to `SUPER_L`
* `J+;` to `KEYPAD_4` and then via xmodmap to `SUPER_R`

In the future I will consider to add also HYPER_L and HYPER_R but for now I'm happy like that. My Vim's LEADER works the same way
* `C+V` to `KEYPAD_5` and the via xmodmap to `NO_BREAK_SPACE`
* `M+;` to `KEYPAD_6` and the via xmodmap to `NO_BREAK_SPACE`

I mapped the Vim's Leader to some strage character that I could never type with a direct key of my keyboard so that I could have leader mappings in insert mode, but that's another story, you could skip this part or you could email me if you wanna know more :smile:


# How to use it

* Install KeyRemap4MacBook
* Go to "Preferences" > "Misc & Uninstall" > "Open private.xml"
* Replace the default private.xml file with the one you find in this repository
* Go to "Change Key"
* Hit "Reload XML"
* A section called "Engelbart" should appear
* Enable the mappings you want to use
* Enjoy :-)


# Last tip

With [PCKeyboardHack](https://pqrs.org/macosx/keyremap4macbook/pckeyboardhack.html.en) I've remapped my `CapsLock` to `Fn` key, so that I can have yet another (sort of) modifier key in my home row! What I do with `Fn`? With KeyRemap4MacBook I've remapped Fn+{H,J,K,L} to... I'll let you guess what :-)
