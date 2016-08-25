Removing Bars
=============

How to remove the menu bar and toolbar on the graphical version of emacs.

Changing .emacs file
--------------------

To remove the menu bar, add the following line inside the `custom-set-variables` function inside
your .emacs file:

```
'(menu-bar-mode nil)
```

Do the same for the following line to remove the toolbar

```
'(tool-bar-mode nil nil (tool-bar))
```

Changing and editing emacs configuration
----------------------------------------

	M-x customize
	Environment
	Frames
	Menu Bar Mode
	     Toggle (to off (nil))
	     State (to save to all future sessions, select option 1)
	Tool Bar Mode
	     Toggle (to off (nil)
	     State (to save to all future sessions, select option 1)

