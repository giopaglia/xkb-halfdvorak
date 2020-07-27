XKB half-dvorak
===============

An annotated half-dvorak keyboard layout for the X Keyboard Extension.

About half-qwerty
-----------------

Half-qwerty is a touch typing technique for one-handed touch typing on
a qwerty keyboard. It has a very gradual learning curve because it
leverages the symmetry of the human hands: right hand finger movements
are mirrored on the left hand and vice versa.

Some older phones have a keyboard marketed as half-qwerty where two
characters, for example Q and W, share the same key. That's obviously
not what we're talking about here.

The technique is decades old and several hard- and software solutions
exists today. [Edgar Matias](https://en.wikipedia.org/wiki/Edgar_Matias)
pioneered the concept and his
[research paper](http://edgarmatias.com/papers/hci96/) on half-qwerty
is an excellent source for further reading on the matter.

About **half-dvorak**
-----------------

As far as I know, there is currently no dvorak counterpart to any half-qwerty layout.
Chances are you ended up here because you were in fact looking for one!
This repo contains the dvorak counterpart of [jorissteyn's half-qwerty layout](https://github.com/jorissteyn/xkb-halfqwerty/).
Compared with that original project, I'm also providing a safe, automated installation process.

Software solutions for Linux
----------------------------

Linux desktop systems use the highly configurable X Keyboard
Extension, or XKB, which can be used to create half-dvorak and half-qwerty layouts.
A well-known half-qwerty configuration for XKB is
[mirrorboard](https://blog.xkcd.com/2007/08/14/mirrorboard-a-one-handed-keyboard-layout-for-the-lazy/)
created by XKCD's Randall Munroe.
The configuration in [jorissteyn's repository](https://github.com/jorissteyn/xkb-halfqwerty/blob/master/halfqwerty.xkb) has some advantages over mirrorboard:

 - the configuration is abundantly annotated
 - it contains a base layout that isn't biased towards a specific
   "flip" modifier and can be cleanly extended
 - it contains a "caps" variant that turns caps-lock into a "flip"
   modifier intended for occasional one-hand typing, similar to
   mirrorboard
 - it contains a "space" variant that optimizes tab and caps-lock for
   using the space bar as flip modifier
 - works well when plugging in and out keyboards of different models
 - can be made available to the keyboard settings of your desktop
   environment
 - tries to be just as friendly to the right hand as it is to the left
   hand
 - tries to mirror as much keys as spatially possible

A noteworthy alternative to handling this in XKB is
[XHK: Xlib HalfKeyboard](https://github.com/kbingham/xhk). It does the
job very well and uses the space bar as a flip switch but it operates on
a lower level which makes it less configurable by design.

Other software solutions for Linux exist but all seem incomplete,
outdated or simply [a bad idea](http://repetae.net/computer/hk/).

Installation
------

```bash
git clone https://github.com/FireSterLine/dvorak-qwerty.git
cd dvorak-qwerty
sudo ./install.sh
```

This will save your xkb configuration (default path: `/usr/share/X11/xkb`) in an archive named xkb-backup-\*.tar.gz, and will apply a patch containing the new configuration files.

Next, the following new keyboard layouts will be available:


+ Dvorak-Qwerty
+ Dvorak-Qwerty simplified (no dead keys)
+ Dvorak-Qwerty, international with dead keys
+ Dvorak-Qwerty alternative international no dead keys
+ Dvorak-Qwerty, classic
+ Dvorak-Qwerty, programmer

You can select them via `setxkbmap` (or your Desktop Evironment settings).

This file is just a front cover, the actual README is the
configuration itself. Start reading it! Some tech-savviness is
required, but you're still here so I guess that's not a problem.


Feedback
--------

Found a bug? Have a better idea?
Unless it's about the installation (which is my real humble addition)
Joris, the [original creator](https://github.com/jorissteyn/xkb-halfqwerty/), would love to hear about it!

Joris Steyn, joris -at- j0r1s.nl

