# neoewm
run xorg without window manager


## linux xorg wtf
maybe you Will find there is 100+ open source xorg window manager there.
how can this be . there must be A reason that writing A Window manager is not that difficult.
but on the other hand , its difficult to write A WM correct.

if the interface is crystal clear and error-proof, then everyone can write A correct WM.
but the facts reversed to prove that the API is A big mess .

so when trying to find A minimum WM. I come to A non-WM.

xorg can make applications and games works good, without A WM.

because of the rubbishing X11 protocol , add A WM can make working one to fail to work .

so, my no-Wm experience seems good enough .

To say A window desktop is ready to work , it should pass some tests.

* run Firefox . you can view YouTube and your favorites .
* run terminal emulator. in my case `Tilix`.
* run text editor . in my case Java swing based `eoeedit`
	A lots of WM fail to show Java swing applications! after investigating , I found the cause is they don't handle `_NET_REQUEST_FRAME_EXTENTS`.
	if you run into A Wm ,search the source for it . if missing , it should not be A earnestness one.
* run `Steam` and the games, like `DOTA2`
* run IDE like `eclipse` and `netbeans`.


## how to 
1. A input event handler read input from /dev/input/*
It's quit low level and before Xorg.

2. I cannot achieve this if I don't run across xdotool.
xdotool is low level than wmctrl.
wmctrl need WM, but xdotool work directly on Xlib.

3.integration 
I found myself A soft engineer rather programmer , when I can take every useful part from other open source software into my own application .

then we bind key to do at lease such things :
* show all Windows in A grid . for navigation .
* focus on A window and make it fullscreen .
* (optional) do more window layouts . like window side by side .


## conclusion 
I did it . 
if you have any question on the steps, just ask .

video:

[![youtube](https://img.youtube.com/vi/RhF2zd0oMYs/0.jpg)](https://youtu.be/RhF2zd0oMYs)








